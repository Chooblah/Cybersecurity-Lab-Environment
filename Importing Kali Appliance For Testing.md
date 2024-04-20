# Step-by-Step Guide: Importing Kali Appliance For Testing

---

## Overview

Configuring the host-only network adapter grants us the ability to test in an isolated environment without affecting other devices on home network. Now, a VM is needed to serve as our 'attacker' VM. For this, a Kali Linux VM will be used. This guide will walk through the process of importing the Kali Linux appliance into VirtualBox.

---

## Prerequisites

Before you begin, make sure you have the following:
- An Active Internet Connection
- A Working Installation of VirtualBox
- A Host-Only Network Adapter Configured in VirtualBox

---

## Steps

### Step 1: Navigating to Kali Linux Downloads Page

**Description:** The first step of this process is going to be navigating to the Kali Linux Downloads page. There are a couple of different selections on the page for different types of downloads. We want to select the option for the Pre-Built VMs.

**Actions:**
1. Open a Browser of Your Choosing
2. Click on the Address Bar and Navigate to https://www.kali.org/get-kali/#kali-platforms
3. Select the Option for "Virtual Machines"

**Screenshots:** 
- ![Screenshot 1](<Screenshots/Importing Kali Linux Appliance For Testing/Navigating-To-Kali-Download-Page.png>)

---

### Step 2: Downloading Kali Linux VirtualBox Appliance

**Description:** Now that we are at the Pre-Built VMs page, we need to be sure that we are selecting a download version that will be compatible with VirtualBox. There will also be both 32-bit and 64-bit download versions. The download the we require is a 64-bit VirtualBox download.

**Actions:**
1. After the Page Loads, Locate the "VirtualBox 64" Box
2. Click The Download Button (Marked in The Screenshot)
3. Wait for the File to Finish Downloading and Extract the Contents to its Own Directory

**Screenshots:** 
- ![Screenshot 1](<Screenshots/Importing Kali Linux Appliance For Testing/Downloading Kali Linux VirtualBox Appliance.png>)

---

### Step 3: Importing Kali Linux Appliance Into VirtualBox

**Description:** After the download of the appliance has finished, we need to import it into our VirtualBox Installation. The VM that we downloaded is pre-configured so there is no pre-configuration changes that need to be made to import the appliance.

**Actions:**
1. Open VirtualBox and Click the Green "Add" Button
2. Locate and Select the File in the Directory with Extracted Contents
3. Click the "Select" Button to Begin the Import

**Screenshots:** 
- ![Part 1](<Screenshots/Importing Kali Linux Appliance For Testing/Importing Appliance Part 1.png>)
- ![Part 2](<Screenshots/Importing Kali Linux Appliance For Testing/Importing Appliance Part 2.png>)

---

### Step 4: Configuring Kali To Use Host-Only Adapter

**Description:** The VM needs to be configured to utilize the host-only adapter we created in the previous guide. This will allow us to conduct testing with the VM in an isolated environment that will not impact any devices that may be using the network your host machine is connected to.

**Actions:**
1. Click on the Imported VM to View the VM Summary Page
2. Locate and Click on the "Network" Tab
3. Confiure the VM to Utilize the Created Host-Only Adapter and Hit the "OK" Button to Confirm Settings

**Screenshots:** 
- ![Part 1](<Screenshots/Importing Kali Linux Appliance For Testing/Configuring Kali To Use Host-Only Part 1.png>)
- ![Part 2](<Screenshots/Importing Kali Linux Appliance For Testing/Configuring Kali To Use Host-Only Part 2.png>)

---

### Step 5: Starting The Kali Linux VM

**Description:** After all of the configurations have been made to the VM, we can now start it to verify proper functionality. We can also test the default credentials to verify that we can log in properly.

**Actions:**
1. Select The Imported VM to View the VM Summary Page
2. Click the Green "Start" Button
3. A New Window Will Appear Displaying the VM

**Screenshots:** 
- ![Part 1](<Screenshots/Importing Kali Linux Appliance For Testing/Starting The Kali Linux VM Part 1.png>)
- ![Part 2](<Screenshots/Importing Kali Linux Appliance For Testing/Starting The Kali Linux VM Part 2.png>)

**Tips:** 
- To Confirm The VM is Using the Host-Only Adapter, Launch a Terminal and use the 'ifconfig' command. The 'inet' address under the 'eth0' interface should display a 172.16.111.x address.

---

## Conclusion

The Kali Linux Virtual Machine that will serve as our 'attacker' machine has been downloaded, imported, and configured. Now, vulnerable Virtual Machines can be downloaded and added to the environment so that we can perform testing on the machines using our Kali Linux VM.

---