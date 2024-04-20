 # Step-by-Step Guide: Installing VirtualBox

---

## Overview

The first part of putting together this homelab is choosing the hypervisor that we are going to be working with. A hypervisor is what serves as our may to monitor and manage the virtual machines that we are going to be running on it. The hypervisor that I have chosen for my homelab is VirtualBox, however options like KVM and VMWare are also popular choices.

## Prerequisites

Before the steps in the below guide can be completed, an active internet connection is required.

## Steps

1. **Step 1: Navigating to VirtualBox Download Page**
    - Description: The first step of the setup is to download the VirtualBox hypervisor software. I started by navigating to the downloads page.
    - Actions:
        1. Open your browser of choice (Chrome, Firefox, Edge)
        2. Click in the address bar, type https://www.virtualbox.org/wiki/Downloads, and hit enter to navigate to the downloads page
        3. Select the link corresponding to the type of Operating System you are running. In my case, Linux.
        ![alt text](Homelab/Screenshots/Installing VirtualBox/Virtual-Box-Downloads-Page.png)
    - Tip: Your setup may vary, depending on which hypervisor you choose.

2. **Step 2: Finding Linux Distro and Version**
    - Description: After Linux has been selected as the OS, I need to specify what distro I am operating on. To find this information, I can open 'Info Center' to view information about my host machine
    - Actions:
        1. Press the super key on keyboard to bring up start menu
        2. Search for and Launch 'Info Center'
        3. Look for information indicating Distro and Version. (Fedora 39)
        ![alt text](/Homelab/Screenshots/Installing VirtualBox/Finding-Fedora-Version.png)

3. **Step 3: Downloading Correct Software Package**
    - Description: There are various different Linux distros and some handle package management differently than others. It is important that the right distro is selected so that our package manager will be compatible with the download.
    - Actions:
        1. On the https://www.virtualbox.org/wiki/Linux_Downloads page, click on the link corresponding to distro
        2. When link is clicked, a download should be initiated for an '.rpm' file
        3. Wait for the download to complete before moving on
        ![alt text](Homelab/Screenshots/Installing VirtualBox/Linux-Downloads-Page.png)

4. **Step 4: Installing VirtualBox Software Package**
    - Description: After the software package has finished downloading, we need to install it so that we can begin using VirtualBox
    - Actions:
        1. After the software package has finished downloading, navigate to the download location
        2. Right Click on the '.rpm' file and click 'Open with Discover'
        3. Click the 'Install' button in the top right corner of the window to begin software package installation
        ![alt text](Homelab/Screenshots/Installing VirtualBox/Virtual-Box-Software-Package.png)
    - Did You Know?: '.rpm' files are Red Hat Package Manager files which are used to store installation files

5. **Step 5: Launching VirtualBox For The First Time**
    - Description: Now that the software package has been downloaded and installed, the software can now be used. Let's launch the application for the first time
    - Actions:
        1. Press the super key on the keyboard to bring up the start menu
        2. Search for and Launch 'VirtualBox'
        3. For ease of access, I usually right click on the app and pin it to task bar.
        ![alt text](Homelab/Screenshots/Installing VirtualBox/Virtual-Box-Initial-Open.png)
    - Tip: A true fresh installation of VirtualBox wouldn't include anything under 'Tools'. I already have some VMs set up

## Troubleshooting

If downloading the software package fails, make sure that you have sufficient space on the storage drive you are installing it on. If it is still failing, verify you have selected the proper Operating System and, if it's Linux, verify you have selected the correct distro.

## Conclusion

System Information was gathered to verify proper VirtualBox software package was downloaded and installed on host machine. Now that the VirtualBox hypervisor software package has been downloaded and installed, it can now be used to create and host VMs.

## Additional Resources

https://www.virtualbox.org/manual/UserManual.html - The VirtualBox User Manual can be a first stop when technical issues come up while utilizing the software.

https://www.virtualbox.org/wiki/Linux_Downloads - Includes additional download options for Linux Distributions