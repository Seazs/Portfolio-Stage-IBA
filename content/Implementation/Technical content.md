---
title: Technical content
draft: 
tags:
---
# **ProteusToolbox core**
As explained in the [[Expected deliverables]] and discuss in the [[Weekly reports]], my main project was the [[Expected deliverables#ProteusToolBox|ProteusToolBox]]. 

To meet the requirements, it was essential to have an efficient way to manage Python environments across different versions.

Several solutions were considered:

## **Using only Conda**

This approach involved creating a new environment for each application to install and using pip to manage installations. However, this method had several drawbacks. Each installation was very slow, and launching applications was also sluggish due to the frequent environment switching required. Furthermore, each environment consumed a significant amount of storage, with many duplicate dependencies even when they were shared across multiple applications (up to 800 MB per application, which quickly becomes impractical with the 30 available apps). Additionally, the Conda Python distribution often included unnecessary libraries, even with Miniconda.

## **Combining Conda and pipx** 

In this setup, Conda was responsible for downloading the Python version, while pipx facilitated easy installation of each application in a dedicated environment using the appropriate Python version provided by Conda. This solution simplified the installation process, and Python versions were only installed once. However, it still faced issues with storage optimization and the heaviness of the Conda distribution.

## **Using pyenv and pipx**

Another consideration was replacing Conda with pyenv, as the pyenv Python distribution is lighter than that of Conda. However, the lack of an official release for Windows made this solution unstable for IBA. Relying on a community-driven project was not a reliable long-term solution.
    
## **Using uv** 

Following the presentation I mention here [[Traces of any evaluations]], a colleague conducted research and found a new Python tool called [uv](https://docs.astral.sh/uv/). This tool consolidates several known tools (such as pyenv, pip, pipx, etc.) by implementing all their functionalities in Rust. Despite being relatively new, it has garnered significant interest. Not only does it combine the capabilities of existing tools, but it also features an optimized storage system for dependencies. It uses a central cache with hard links (multiple file pointers to the same data on disk), functioning similarly to the central repository in Maven. Each new environment that requires already downloaded dependencies will simply create a hard link to the existing data. This approach significantly reduces the storage footprint of installed applications, given that many common libraries (such as NumPy, Matplotlib, and PyQt) are often reused.


# **ProteusToolBox applications repository**

The Software Department at IBA uses Nexus repositories to store Java and Python packages. This online server allows for the storage of private code and facilitates easy distribution to other IBA members. It notably enables the storage of Python packages.

We have decided that the Python applications intended for the ProteusToolBox should be packaged as Python packages and published in a dedicated repository for the ProteusToolBox. This approach allows us to easily display and provide a precise list of applications available for download using the Nexus API. This API supports a range of operations, such as listing a specific repository and retrieving various pieces of information about the packages contained within it.



# **Publishing application to the ProteusToolbox**

As mentioned above, to be available in the proteusToolbox, application package must be published on the Nexus repository.Given that some of the developers of these applications are more physicists than software engineers, we aimed to simplify the process of publishing and updating applications.

To achieve this, we created predefined GitLab CI pipeline jobs that developers can easily add to their projects. **GitLab CI (Continuous Integration) pipelines are automated processes that allow developers to run tests, build applications, and deploy code automatically when changes are made to a project. They streamline the software development lifecycle by ensuring that code changes are tested and validated before being merged into the main codebase.**

These generic jobs ensure that the package structure is correct and that all necessary information for the ProteusToolBox is included. Once verified, they publish the package to the Nexus repository after receiving approval from Adrien, who only needs to perform a simple operation to initiate the upload. Since he is the non-product software owner, this process allows him to maintain control over what gets published in the ProteusToolBox and is available for download by other users of the application.

While the control process was still minimal during my time there, the goal was to implement more robust checks for non-product software (NPS). However, this depends on each program, as it’s necessary to analyze the risks associated with using an NPS. For instance, if an NPS encounters an error, we need to have a mechanism in place to detect it reliably.



# Generic windows installer for python application

As explained [[Expected deliverables]], the target users are not necessarily software engineers. It was therefore important to provide a Windows installer that would allow for easy, graphical installation of the ProteusToolBox.

With the discovery of [uv](https://docs.astral.sh/uv/), I realized the possibility of creating Windows installers for any Python application.

Since uv can install an application in a dedicated environment, along with the required Python version if necessary, creating an installer for any application became achievable. I developed a PowerShell script that takes the name and version of the Python package as parameters. Then, uv handles installing the Python version, creating a dedicated environment, and installing the application (the package) within it.

I linked this PowerShell script to an Inno Setup script. **Inno Setup** is a tool for creating Windows installers that enables users to easily install, update, and remove applications through an intuitive interface. It compiles the files and dependencies into a single executable installer, making distribution straightforward.

I then packaged all of this into a Python package, allowing me to create an installer for any Python application.

This package is used in the CI pipeline for the ProteusToolBox to create a Windows installer for each new official release (though not strictly necessary, as the application has an auto-update feature). This package was also used in my supervisor's project to generate a dedicated Windows installer, allowing it to be installed independently of the ProteusToolBox (useful for users who may only need a single application, making it more convenient).