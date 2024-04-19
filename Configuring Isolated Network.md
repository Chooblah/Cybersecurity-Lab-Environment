# Step-by-Step Guide: Configuring Isolated Network

---

## Overview

After the hypervisor has been installed, an isolated network environment for the VMs needs to be created. This can be done by creating a host-only network adapter for the VMs to utilize. The 'Host-Only' network adapter creates a network where the VMs can interact with the host and other VMs utilizing that adapter only. VMs utilizing a host-only network adapter cannot communicate out to the internet.

## Prerequisites

Before you begin, ensure you have the following:
- A Working Installation of VirtualBox

## Steps

### Step 1: Navigating To Network Manager

![Step 1 Image](Homelab/Screenshots/Configuring Isolated Network/Navigating-To-Network-Manager.png)

**Description:** When VirtualBox is opened for the first time, we are greeted with the "Welcome To VirtualBox" Screen. We need to navigate to the Network Manager, where we can then create the host-only network adapter.

**Actions:**
1. Open VirtualBox
2. Click on the 'Hamburger' button located on "Tools"
3. Locate and Click the "Network" option to open the Network Manager

---

### Step 2: Creating Host-Only Network Adapter

![Step 2 Image](Homelab/Screenshots/Configuring Isolated Network/Creating-Network-Adapter.png)

**Description:** After Network Manager has been opened, we can then create, select, and view the default settings of the newly created network adapter. 

**Actions:**
1. Click the "Create" button to create the new host-only network adapter
2. Click on the newly created network adapter, selecting it and allowing us to view adapter configuration information
3. Configure the adapter to mimic the configuration in the screenshots. 

---

### Step 3: Configuring Network Adapter

![Configuration Tab 1](Homelab/Screenshots/Configuring Isolated Network/Adapter Settings Part 1.png)
![Configuration Tab 2](Homelab/Screenshots/Configuring Isolated Network/Adapter Settings Part 2.png)

**Description:** There are two parts to configuring a newly created host-only network adapter. First, we need to specify that we want to configure the adapter manually, and the next part is configuring the DHCP server. After the adapter has been configured, it is ready for VMs to utilize!

**Actions:**
1. Configure the "Adapter" tab to match the configuration shown in Image 1
2. Configure the "DHCP" tab to match the configuration shown in Image 2

**Tips:** 
- When configuring the adapter, make sure to configure one tab at a time and hit 'Apply' after changes have been made

---

## Troubleshooting

Here are some common issues you might encounter and how to solve them:

- **Issue 1:** If you attempt to configure the adapter settings and you receive an error when attempting to enter an address in the 172 range, you may need to make additional configurations to your host system. If directory /etc/vbox doesn't exist, create it. Then, create a file called 'networks.conf' and add the line '* 172.16.0.0/12' to the file. You may need to reboot the system but this will allow you to make the necessary adapter configurations.

## Conclusion

Now that the host-only network adapter has been created, it is ready to be utilized by any VMs that are added to the lab. This allows a safe and isolated environment where testing and analysis can be performed without disrupting anyone that may be utilizing your home network. 