## Bash pipeline

### Bash automation is simple and delivers any job scripted to perform. I love it because it touches on the process/pid of a task.

### github repo
[automation](https://github.com/aiegoo/automation)

### udemy course list
- Linux shell scripting: a project based approach to learning [udemywiki](https://github.com/aiegoo/udemy/wiki/devop3)
- Bash shell scripting and automation [udemywiki](https://github.com/aiegoo/udemy/wiki/devop26)
- Intro to linux shell scripting [udemywiki](https://github.com/aiegoo/udemy/wiki/devop29)

Below is codebase I've been working on since October 2019, eventually ended up in an app called Spire. From stage 1 (https://github.com/aiegoo/automation/wiki/Stage1), stage 2 (https://github.com/aiegoo/automation/wiki/stage2) to Spire (master branch), overwriting contents has become sophisticated and its codes are wrap up into a single executable file.  Here is the instruction how to set up for demonstration;
<hr>
<hr>

# Spire
A Very Simple Automation/Command & Control Solution

# Overview
Spire was designed to be flexible, extensible, fast and also easy to set up, use and understand.
It is extremely portable because it is fully confined to a single directory.
For configuration, it uses a combination of YAML and plaintext files.

Spire consists of two programs: 
- server-update
- slave

# server-update
Server-update takes two arguments:

- Slave group containing a list of slaves to send requests to
- Name of the script file which the slaves should look for and execute

All slaves, along with groups which they belong to, are specified in a <i>slavelist.yaml</i> file.

# slavelist.yaml
<i>Slavelist.yaml</i> file is parsed by server-update in order to determine which slaves to send a POST request to.
The file is organized as a list of groups, each having a name and a list of slaves which belong to that group.

For example:

```
---
groups:
 - name:	Local
   slaves:
    - ip:	http://127.0.0.1
    - ip:	http://localhost

 - name:	Remote
   slaves:
    - ip:	http://example.com
...
```

It is possible to, for example, run a script called example.sh only on the Local group by running:

```
./server-update Local example.sh
```

Alternatively, it is possible to, instead of specifying a group name, tell the program to run a certain script on all groups like so:

```
./server-update all example.sh
```

# slave
Slave is a web server which listens on port 10000.
Slave can send and receive data only through a POST request. The data it receives is a script name which it then looks for in the Scripts folder, located within the same directory as the slave program itself. If it finds the script in question, it will attempt to execute it within a separate process. If it succeeds, it will notify the sender that the script was executed successfully; Alternatively, it will notify the sender that something went wrong or that the script in question was not found.

It is important to note that all scripts should have a proper #! line, along with executable permissions. If they do not, the slave will catch and log an error.

# secret.txt
<i>Secret.txt</i> file should be filled with arbitrary, random data supplied by the user. It is used for secure hashing of data which is to be transmitted over the network. It should be located within the same directory as the programs.

Server-update transmits data in a form of a SHA256 hash. When a script name is specified, for example <i>example.sh</i>, the name is concatenated with the contents of the local <i>secret.txt</i> file.
A SHA256 hash is then made out of the aforementioned combination and sent to the slave via a POST request.

The slave receives the SHA256 hash. It then reads its own secret.txt file and begins going through all of the scripts in the Scripts folder. It concatenates the contents of its own <i>secret.txt</i> file with each script name it finds in the Scripts folder. If it finds a SHA256 hash that matches the one sent to it via the POST request, it knows that it has found the script which it should execute.

<b><i>For this exchange to work, secret.txt files should be identical on both the server-update side and on the slave side. If they are not, the slave will never find a matching hash and will, therefore, notify the sender that it was unable to find the script in question, even if that script really exists.</i></b>

# tl;dr

The files needed for server-update are:
- slavelist.yaml
- secret.txt

The files and folders needed for slave are:
- Scripts (folder)
- Script files within the Scripts folder (with proper permissions and #! lines)
- secret.txt

Both secret.txt files on the server-update side and the slave side should be identical.
All files should be located within the same directory as the programs.