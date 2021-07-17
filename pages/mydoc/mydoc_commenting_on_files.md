---
title: Commenting on files
tags:
  - navigation
keywords: "annotations, comments, feedback"
last_updated: "November 30, 2016"
summary: "You can add a button to your pages that allows people to add comments."
sidebar: mydoc_sidebar
permalink: mydoc_commenting_on_files.html
folder: mydoc
---

## pixhaw4

| Type  | Details | Type  | Details |
| :---: | ---  | :---: | ---  |
| frame |  | FC |  |
| motor |  | ESC |  |
| RC  |  | mode |  |
| weight |  | class |  |
| battery |  | air-time |  |
| configurator |  |  last updated |   |


## Brief Introduction to Experimental Platforms

Platform Composition
------------------------

The experimental platform is a rapid development platform for multicopter control
algorithm design based on MATLAB/Simulink and Pixhawk. It is mainly composed
of the following five parts: the Simulink-based Controller Design and Simulation
Platform, the HIL Simulation Platform, the `Pixhawk Autopilot System <https://docs.px4.io/master/en/flight_controller/pixhawk_series.html>`_ ,
the Multicopter Hardware System, and the Instructional Package.

(1). Simulink-based Controller Design and Simulation Platform

As shown in Fig. 3.1, this platform has a high-fidelity nonlinear model for simulating 
various multicopter dynamics. Furthermore, there is an interface for communicating 
with the FlightGear simulator to provide a real-time 3D display for
the flight status (e.g., trajectory and attitude) of the simulated multicopter. 
Multicopter control algorithms can be conveniently designed on this Simulink-based
simulation platform and then verified with SIL simulations. Furthermore, the
Pixhawk Support Package (PSP) toolbox can be used to generate C/C++ code
of the control algorithms, which is then compiled and uploaded to a Pixhawk
autopilot.

![](https://rflysim.com/en/_images/Quan-ch3-Fig3.1.jpg)

    .. figure:: /images/Quan-ch3-Fig3.1.jpg
        :align: center

        Fig. 3.1 Simulink-based controller design and simulation platform

(2). HIL Simulation Platform

The HIL simulation platform includes a real-time motion simulation 
software�봀opterSim (see Fig. 3.2a) and a 3D visual display software��3DDisplay (see
Fig. 3.2b). The simulation model of CopterSim is obtained by importing 
parameters from the Simulink-based simulation platform mentioned earlier. Both
CopterSim and 3DDisplay must run on a computer with Windows OS (Win7
or higher, x64). They are connected with the Pixhawk autopilot through a USB
cable, thereby establishing a closed-loop control system for HIL simulations.


![](https://rflysim.com/en/_images/Quan-ch3-Fig3.2.jpg)

    .. figure:: /images/Quan-ch3-Fig3.2.jpg
        :align: center

        Fig. 3.2 HIL simulation platform

(3). Pixhawk Autopilot System

Figure 3.3 illustrates the entire Pixhawk autopilot system that includes a
Pixhawk autopilot, an RC transmitter, an RC receiver, and a Ground Control
Station (GCS). The Pixhawk autopilot used in this book is composed of 
Pixhawk 1 (2MB flash version) [#f2]_ autopilot hardware and PX4 autopilot software.
The PX4 autopilot software [#f3]_ has a built-in Real-Time Operating System (RTOS)
to ensure basic functions, such as multi-thread scheduling, low-level drivers, and
algorithm execution. The Pixhawk autopilot uses an RC receiver to wirelessly
connect with the corresponding RC transmitter for receiving the control commands 
from the remote pilot on the ground. Further, the Pixhawk autopilot can
also wirelessly connect with GCS through a pair of radio telemetry to exchange
flight data and mission commands.


![image](https://user-images.githubusercontent.com/42961200/126034081-5bfe5ebe-d879-462d-bafb-8d0868ac3ac7.png)

    .. figure:: /images/Quan-ch3-Fig3.3.jpg
        :align: center

        Fig. 3.3 Pixhawk autopilot system

(4). Multicopter Hardware System

As shown in Fig. 3.4, a multicopter hardware system is usually composed of
an airframe system, a propulsion system, external sensors, a test stand, etc.
Combining the Pixhawk autopilot and a multicopter hardware system requires
an integrated multicopter flight platform that can be used to perform specific
flight tasks. According to the actual flight performance requirements, the 
multicopter airframe system can be designed with different configurations, such as
quadcopters, hexacopters, and coaxial octocopters. In this book, a small quadcopter 
is chosen as an example to study its hardware system design, such as
airframe design, propulsion system selection. Then, the control algorithms are
designed for the resulting multicopter hardware system.

![](https://rflysim.com/en/_images/Quan-ch3-Fig3.4.jpg)


    .. figure:: /images/Quan-ch3-Fig3.4.jpg
        :align: center

        Fig. 3.4 Multicopter hardware system

(5). Instructional Package

This book encompasses video tutorials, PowerPoint files, and source code examples. 
The topic is closely related to our previous book [#f8]_.

Platform Advantage
----------------------

This experimental platform provides interfaces for multicopter controller design in
MATLAB/Simulink. Readers (beginners, students, or engineers) can develop a rapid
design and verify the control algorithms by SIL simulation. After the control 
algorithms are well designed and verified, the platform also provides a code generation
function to generate Simulink controllers to C/C++ code. Then, the code can be 
compiled into the autopilot software firmware file; finally, it is automatically uploaded
to the Pixhawk hardware. The platform also provides a HIL simulation platform
for preliminary simulation tests on a Pixhawk autopilot system that may help in
eliminating potential problems that may exist in flight tests. After all the tests are
completed, indoor and outdoor flight tests can be carried out by assembling the Pixhawk 
autopilot onto a real multicopter hardware system. The performance of the
designed controllers can be evaluated through experimental tests.

.. rubric:: References
.. [#f2] corresponding to the circuit diagram version Pixhawk 2.4.6; for more details, please visit this website: https://docs.px4.io/master/en/flight_controller/pixhawk.html.
.. [#f3] In addition to supporting the PX4 autopilot software used in this book, the Pixhawk series autopilots also support Ardupilot open-source autopilot software; see: http://ardupilot.org/dev/index.html.
.. [#f8] 짤 Publishing House of Electronics Industry 2020 Q. Quan et al., Multicopter Design and Control Practice, https://doi.org/10.1007/978-981-15-3138-5_3



<hr>

2. Simulink-Based Controller Design and Simulation Platform
To improve the design efficiency of multicopter controllers, as shown in Fig. 3.5, this book provides a high-fidelity simulation environment based on Simulink/FlightGear. The main source code file is presented in “e01.SoftwareSimExps CopterSim3DEnvironment.slx”.

![image](https://user-images.githubusercontent.com/42961200/126034282-e9ca908c-7792-441b-afee-5f388215ad7d.png)


../_images/Quan-ch3-Fig3.5.jpg
Fig. 3.5 Files in “SoftwareSimExps” folder

The following steps describe the correct way to open Simulink files (those with the file suffix “.slx”).

(1). Open MATLAB via the Windows desktop shortcut or the Windows start menu. (2). As shown in Fig. 3.6, click the “Browse Folder” button in the MATLAB User Interface (UI) to set the current directory to the folder of the “.slx” file to be opened.

![image](https://user-images.githubusercontent.com/42961200/126034306-c3a10305-f15d-433f-8c21-e7000cfd82c6.png)


../_images/Quan-ch3-Fig3.6.jpg
Fig. 3.6 Method to correctly open a Simulink slx file

(3). Double-click the “.slx” file in the “Current Folder” window (the lower-left side in Fig. 3.6) to open it.

All “.slx” files should be opened in this way to ensure that the working directory is correct and that the initialization scripts are successfully loaded.

![image](https://user-images.githubusercontent.com/42961200/126034308-0429575c-2c71-4933-aea9-d635bfc80f67.png)


../_images/Quan-ch3-Fig3.7.jpg
Fig. 3.7 Simulink SIL simulation example

Open the “CopterSim3DEnvironment.slx” file according to the above procedure; then, a SIL simulation example will appear as shown in Fig. 3.7. The SIL simulation example contains three subsystems: the “Controller” subsystem, the “Multicopter Model” subsystem, and the “FlightGear Interface” subsystem. Their key features are summarized below.

(1). The input, output, and feedback signals of the “Controller” subsystem are consistent with the available signals in a real autopilot system. For example, the input signals of the controller in Fig. 3.7 are the control commands for pitch, roll, yaw, and altitude control from a simulated RC transmitter, and the output signals are the motor PWM signals for a multicopter model.

(2). The controller uses the sensor estimated states (e.g., attitude, angular velocity, position, velocity, and other state information) to achieve stable attitude control.

(3). The input and output signals of the “MulticopterModel” subsystem are consistent with those of a real multicopter. For example, the input signals of the “Multicopter Model” subsystem are the PWM control signals of eight motors (the multicopter model will choose the actual number of motors according to the selected model) defined by the Pixhawk autopilot (the data range is 1000–2000 corresponding to a throttle command of 0–1), and the output signals are the data from various sensors.

(4). “FlightGear Interface” subsystem provides a communication interface to send the flight data to FlightGear, where the real-time vehicle attitude and flight trajectory can be observed in a realistic 3D scene.

2.1. Controller
Double-click the “Controller” subsystem in Fig. 3.7 yields the internal structure of the controller, as presented in Fig. 3.8. This example shows a simple attitude controller for pitch and roll angles. The controller receives the control signals from the RC transmitter and controls the multicopter to achieve the desired pitch and roll angles.

As shown in Fig. 3.8, the 1st–5th input ports are five input channels from the RC transmitter (“ch1”–“ch5”); the 6th–8th input ports are the angular velocity (“p”, “q”, “r”) from the gyroscope sensor; the 9th–10th input ports are the roll angle and pitch angles (“phi”, “theta”) estimated from the inertial sensor. As shown in Fig. 3.8, the computing process of the entire “Controller” subsystem is roughly divided into five steps.

![image](https://user-images.githubusercontent.com/42961200/126034319-a160b15b-fcc1-4586-bfc1-df62371d2783.png)

../_images/Quan-ch3-Fig3.8.jpg
Fig. 3.8 Internal structure of “Controller” subsystem

(1). The “Input Interfaces” module receives the RC transmitter signals and the multicopter state estimation signals. [1]

(2). The “RC Signal Process” module maps the five-channel signals of the RC transmitter to the desired roll and pitch angle values.

(3). The “Attitude Controller” module computes the desired force and torque values to control the multicopter to the desired attitude.

(4). The “Motor Control Signal Computation” module maps the force and torque values to the control signals (ranging from 1000 to 2000) for the four motors.

(5). The “Output Interfaces” module fills the remaining 4-dimensional control signals and generates an 8-dimensional PWM signal (there are eight PWM output ports on Pixhawk) ranging from 1000 to 2000µs. [2]

2.2. Multicopter Model
Double-click the “Multicopter Model” subsystem in Fig. 3.7, and the internal structure of the multicopter model is presented in Fig. 3.9. The multicopter model simulates a real multicopter system to output the flight state and sensor signals based on the motor PWM controls from the control system.

![image](https://user-images.githubusercontent.com/42961200/126034338-c744a55b-3fe7-4f86-ae93-f7694bc20e60.png)

../_images/Quan-ch3-Fig3.9.jpg
Fig. 3.9 Internal structure of “Multicopter Model” subsystem

As shown in Fig. 3.9, the “Multicopter Model” subsystem contains the following seven main modules.

(1). “Motor Model” module: it simulates the motor dynamics.

(2). “Force and Moment Model” module: it simulates all external forces and moments acting on the body, such as the propeller thrust, fuselage aerodynamics, gravity, and ground supporting force.

(3). “Rigid Body Kinematics Model” module: it calculates the vehicle kinematics of the multicopter, such as speed, position, and attitude.

(4). “Environmental Model” module: it calculates the environmental data, such as gravitational acceleration, air density, wind disturbances, and geomagnetic field.

(5). “Fault Model” module: it is mainly used to inject model uncertainties (related to mass and moment of inertia) as well as faults.

(6). “Battery Model” module: it simulates the discharge process of the battery.

(7). “Output Interface Model” module: it packs the output signals in the desired format.

The controller parameters are stored in an initialization script “e01.Software SimExpsInit_control.m”. This script will be automatically called to import all parameters into the Simulink workspace when the simulation starts. Figure 3.10 depicts how to proceed to autorun the initialization script. Readers can open the UI in Fig. 3.10 by clicking “File”—“Model Properties”—“Callbacks”—“InitFcn” in the Simulink menu within the “CopterSim3DEnvironment.slx” project. The source code of the “Init_control.m” initialization script is listed in Table 3.1.

![image](https://user-images.githubusercontent.com/42961200/126034353-82315d15-0090-439e-b2fd-dc752b2fd7b7.png)

../_images/Quan-ch3-Fig3.10.jpg
Fig. 3.10 Initialization interface for the “Init_control.m” script

All the parameters required by the “Multicopter Model” are stored in the script “e01.SoftwareSimExpsiconInit.m”. This script will be automatically called when the second line (see Table 3.1) of the “Init_control.m” script is executed. The key model parameters are listed in Tables 3.2, 3.3, 3.4, 3.5, and 3.6. By modifying the above model parameters, multicopters with different sizes and configurations (see Table 3.5) can be obtained, and flight simulations under different environments (see Table 3.6) can be performed.

2.3. FlightGear Interface
As shown in Fig. 3.7, the “FlightGear Interface” subsystem has three input ports representing the multicopter position, Euler angles, and motor PWM signals, respectively. This subsystem sends multicopter flight state information to FlightGear to observe the flight attitude and trajectory of the multicopter in a 3D scene. The steps to follow are described next.

(1). Double-click the FlightGear-F450 shortcut on the desktop to open FlightGear;

(2). Click the “Run” button on the Simulink toolbar (see Fig. 3.11) to run the “CopterSim3DEnvironment.slx” file;

![image](https://user-images.githubusercontent.com/42961200/126034368-1561e59d-3a9f-4079-9c7a-c8806e7a8997.png)


../_images/Quan-ch3-Fig3.11.jpg
Fig. 3.11 Simulink “Run” button for different MATLAB versions

(3). Then, as shown in Fig. 3.12, the multicopter takes off vertically from the ground and starts flying forward at a certain pitch angle after 5 s.

![](https://rflysim.com/en/_images/Quan-ch3-Fig3.12.jpg)


<hr>
<hr>


## About the review process

If you're using the doc as code approach, you might also consider using the same techniques for reviewing the doc as people use in reviewing code. This approach will involve using Github to edit the files.

There's an Edit me button on each page on this theme. This button allows collaborators to edit the content on Github.

Here's the code for that button on the page.html layout for GitHub:

```
{% raw %}{% if site.github_editme_path %}

<a target="_blank" rel="noopener" href="https://github.com/{{site.github_editme_path}}/{{page.folder}}{{page.url | append: ".md"}}{% endif %}" class="btn btn-default githubEditButton" role="button"><i class="fa fa-github fa-lg"></i> Edit me</a>

{% endif %}{% endraw %}
```

and here for GitLab:


```
{% raw %}{% if site.gitlab_editme_path %}

<a target="_blank" rel="noopener" href="https://github.com/{{site.gitlab_editme_path}}/{{page.folder}}{{page.url | append: ".md"}}{% endif %}" class="btn btn-default githubEditButton" role="button"><i class="fa fa-gitlab fa-lg"></i> Edit me</a>

{% endif %}{% endraw %}
```

In your configuration file, edit the value for `github_editme_path` (or for Gitlab: `gitlab_editme_path`). For example, you might create a branch called "reviews" on your Github repo. Then you would add something like this in your configuration file for the 'github_editme_path': tomjoht/documentation-theme-jekyll/edit/reviews. Here "tomjoht" is my github account name. The repo name is "documentation-theme-jekyll". The "reviews" name is the branch.

To suppress this button, comment out the `github_editme_path` in the \_config.yml file.

## Add reviewers as collaborators

If you want people to collaborate on your project so that their edits get committed to a branch on your project, you need to add them as collaborators. For your Github repo, click **Settings** and add the collaborators on the Collaborators tab using their Github usernames.

If you don't want to allow anyone to commit to your Github branch, don't add the reviewers as collaborators. When someone makes an edit, Github will fork the theme. The person's edit then will appear as a pull request to your repo. You can then choose to merge the change indicated in the pull or not.

{% include note.html content="When you process pull requests, you have to accept everything or nothing. You can't pick and choose which changes you'll merge. Therefore you'll probably want to edit the branch you're planning to merge or ask the contributor to make some changes to the fork before processing the pull request." %}


## Workflow

Users will make edits in your "reviews" branch (or whatever you want to call it). You can then commit those edits as you make updates.

When you're finished making all updates in the branch, you can merge the branch into the master.

Note that if you're making updates online, those updates will be out of sync with any local edits.

{% include warning.html content="Don't make edits both online using Github's browser-based interface AND offline on your local machine using your local tools. When you try to push from your local, you'll likely get a merge conflict error. Instead, make sure you do a pull and update on your local after making any edits online." %}

## Prose.io

 Prose.io is an overlay on Github that would allow people to make comments in an easier interface. If you simply go to [prose.io](http://prose.io), it asks to authorize your Github account, and so it will read files directly from Github but in the Prose.io interface.

 {% include links.html %}
