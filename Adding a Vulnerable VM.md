# Step-by-Step Guide: Adding a Vulnerable VM

## Introduction

In our current virtual environment, there is only a Kali Linux VM that will serve as our 'attacker'. Other VMs need to be added to the environment to allow us to perform testing. I will be utilizing pre-configured vulnerable VMs from the Vulnhub website.

## Prerequisites

Before you begin, make sure you have the following:
- An Active Internet Connection
- A Working Installation of VirtualBox
- A Host-Only Network Adapter Configured in VirtualBox

## Steps

### Step 1: Navigating to Vulnhub Website

During this step, we need to navigate the the Vulnhub website where we will download the vulnerable VMs. Vulnhub has a collection of vulnerable VMs that range in difficulty and complexity.

**Actions:**
1. Open a Browser of Your Choice
2. Click on the Address Bar and enter https://www.vulnhub.com/
3. Hit the 'Enter' key to navigate to Vulnhub website

![Step 1 Screenshot or Image](step1_image.png)

---

### Step 2: Searching For and Selecting Vulnerable VM

After we have navigated to the Vulnhub website, we need to find the VM that we are going to use for testing. In this example, I searched for the Metasploitable 2 VM, as this serves as a good beginning learning machine.

**Actions:**
1. Click on the Search Bar and Enter 'Metasploitable 2'
2. Hit Enter to Search
3. Click on the Option for Metasploitable: 2

![Step 2 Screenshot or Image](step2_image.png)

---

### Step 3: Downloading Vulnerable VM

Selecting the VM from the search or home page will bring you to that VMs summary page. This will include various details about the VM, including download links for the VM files. We need to download the VM files so they can be added to our virtual environment.

**Actions:**
1. Locate the 'Downloads' Links on the VM Summary Page
2. Click a Valid Download Link to Begin the Download
3. Wait for the Download to Complete

![Step 3 Screenshot or Image](step3_image.png)

---

### Step 4: Adding Vulnerable VM to VirtualBox

A VM needs to be created in VirtualBox with default settings and without an attached storage drive. This will be the VM that we add the contents downloaded from the Vulnhub website. We will add the virtual drive to the machine later.

**Actions:**
1. Open VirtualBox and Select the Blue 'New' Button
2. Configure the VM Using the Same Config in the Screenshots Provided
3. Click the "Finish" Button to Finalize the Creation of the VM

![Step 3 Screenshot or Image](step3_image.png)

---

### Step 5: Adding VM Virtual Disk

After the files have finished downloading from Vulnhub, they need to be extracted from the compressed folder. The virtual disk file must then be attached to VirtualBox so it can be added to the VM we created in the last step.

**Actions:**
1. Extract the Downloaded Contents from Vulnhub
2. Open the "Media" Section in VirtualBox
3. Add Virtual Disk File Using Screenshots Provided

![Step 3 Screenshot or Image](step3_image.png)

---

### Step 6: Configuring VM Storage

Now that the virtual disk file has been added to VirtualBox, we need to configure the newly created VM to utilize that virtual disk file.

**Actions:**
1. Click on the Vulnerable VM to View VM Summary
2. Click on the "Storage" Tab 
3. Add the Virtual Disk to VM Using Provided Screenshots

![Step 3 Screenshot or Image](step3_image.png)

---

### Step 7: Configuring VM Network Adapter

In order for the VM to communicate with our Kali 'attacker' VM, it needs to be on the same network. The newly created VM needs to be configured to use the same host-only adapter that the Kali VM is utilizing. All VMs added in the future need to also utilize this adapter, in order to communicate with Kali.

**Actions:**
1. Click on the Vulnerable VM to View VM Summary
2. Click on the "Network" Tab 
3. Configure VM to Utilize Created Host-Only Network Adapter Using Same Steps as Last Guide

![Step 3 Screenshot or Image](step3_image.png)

---

### Step 8: Starting VM In Headless Mode

Starting the VM in headless mode will prevent a separate window opening to display the VM. Instead, the VM will run in the background. We run the vulnerable VMs in this mode because we won't need to do any interacting with the VM directly. All of the interaction with the vulnerable VMs should be able to be done with the 'attacker' VM.

**Actions:**
1. Click on the Vulnerable VM to View VM Summary
2. Click on the Tiny Down Arrow Next to the Green "Start" Button
3. Click on "Headless Start" to Start VM in Headless Mode

![Step 3 Screenshot or Image](step3_image.png)

---

## Conclusion

Our virtual testing environment is now fully complete with an attacker machine and a vulnerable machine to perform testing on. This environment can be easily scaled to fit your needs as they grow with experience. More VMs can be added both from Vulnhub and other sources using a similar method as the one described in this guide.

---