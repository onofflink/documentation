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

===============================================
Brief Introduction to Experimental Platforms

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

![](https://rflysim.com/en/_images/Quan-ch3-Fig3.2.jpg)

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

![](![Uploading image.png…]()
)

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
