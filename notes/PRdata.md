# Programming Renaissance Environment

Initially, <abbr title='Programming Renaissance'>PR</abbr> will run on Linux and the following sections describe the basic configuration of the data used within PR. However, it is intended that PR will run on Windows as well, either stand-alone or in a dual boot with Linux enviroment.<br>
Initial development will be on the Ubuntu distribution - version 22.10.

## Organization

This document talks about partitions. The system might have a single disk with multiple partitions or several disks, each with one or more partitions.

### Linux Boot Disk

This disk partition contains the Linux operating system. It is intended that Linux can be reinstalled without losing any programs or data that have been installed after the original system installation.

### Linux User Data

This disk partition contains user data that is
specific to Linux as well as operating system directories thatshould not be affected by a re-installation of the operating systems. At least it will contain the /home and the /usr/local directories.

### Shared Data

This disk contains the majority of the user data and will be shared between Linux and Windows in a dual boot environment or when Windows runs in a virtual machine.

## Programming Renaissance Data

The majority of this data will be stored in the Shared Data partition, but operating system dependent data will be stored in the relevant  operating system dependent User Data partitions.

### PR Data Structure

The directory structure will be the same both in the Shared Data partition and in the operating system specific User Data partitions. The following will be the initial structure.

The root directory will be called ProgrammingRenaissance. It will contain sub-directories with the major concerns of PR. Initially, the following areas will be covered:
administration, projects, members and website.

#### Administration

This area is concerned with everything needed to run the PR organization.

#### Projects

These are the main concern of PR. Most development work will take place here. There will be one sub-directory for each project that PR is working on.

#### Members

PR will offer each member a private area within a PR component to hold personal data and to support a personal website. This is the place for personal material that should be kept private but it can still take part in the infrastructure offered to each PR member.

#### Website

This area contains the source material and the working material for the PR organization. The website will be initially hosted on [Github Pages](https://pages.github.com/) but can also be displayed locally on a member's computer for testing purposes. The website is generated and maintained using [Jekyll](https://jekyllrb.com/).

Within each area, the following structure will apply:
* Notes<br>
  This area is used for notes that contain thoughts about ongoing development. They are informal and provide a place to record ongoing thinking as it happens. This is where the original thinking for a tool or project takes place.
* Scripts<br>
  These are tools that facilitate the operation of each area within PR. They are typically bash scripts on Linux and Powershell scripts on Windows but they are not restricted to those languages if others do a better job in particular circumstances.
* Source Management<br>
  Initially, this will be a Git repository. There will be one repository for ech major area, so individual repositories will be kept reasonably small. 
* Deployment<br>
  This section will contain scripts that are specialized in deploying tools and projects to the point of use for internal tools, or to the user facing repositories that support distribution of PR projects to the public.
* Documentation<br>
  This section will contain the formal  documentation for each project or internal content of the PR organization.

## Programming Renaissance Projects

This is where the majority of the PR activity takes place. There is one section under this heading for each item that is being developed by PR.