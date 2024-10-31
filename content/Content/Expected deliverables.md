---
title: Expected deliverables
draft: 
tags:
---
# ProteusToolBox
The main deliverable of this internship is the ProteusToolbox application. This store and launcher for python application was initially designed primarily for flying engineers. These engineers works on site and are responsible for the maintenance and upkeep of hospital machinery. They rely on several Python applications to automate certain tasks. Before the development of ProteusToolbox, each application had to be installed individually, which posed a significant challenge, as installing Python applications can be complex. This was especially burdensome for engineers who often work on hospital computers, requiring them to repeat installations at each new site.

This need led to the creation of ProteusToolbox, a store that simplifies the installation of a predefined list of Python applications by proposing a graphical interface. Espetially knowing that the users aren't necessarily familiar with terminal commands.

However, the first version of ProteusToolbox is limited by a fixed version of Python and locked dependencies, which can constrain other applications that may require different versions.

The goal of this internship deliverable is thus an enhanced version of ProteusToolbox, where each application has its own dedicated Python environment, removing restrictions related to Python versions and dependencies.

In parallel with the application, the goal was also to automate several processes to enhance usability and streamline updates, including:

- **Simplified Installation**: Providing a Windows installer for easy setup of ProteusToolbox.
- **Automated Development Processes**:
    - Automating the testing of the application to ensure consistent functionality and quality.
    - Setting up automatic deployment for seamless updates.
    - Streamlining the publication process for new applications within ProteusToolbox.

These enhancements aim to improve the overall user experience and reduce the manual workload for engineers.


Here is some screenshot of the application in it's final form at the end of my internship. (**confidential**)

This is the main menu from which you can see and launch installed application
![[Capture d'écran 2024-10-29 165216.png]]


Here is for exemple when the application Ftov-Editor is launched
![[Capture d'écran 2024-10-29 165805.png]]


Here is the store that directly fetch all available application on a Nexus repository
![[Capture d'écran 2024-10-29 165618.png]]

And here is the menu where you can change the Nexus repository to either select the development or production server. 
![[Capture d'écran 2024-10-29 165540.png]]



