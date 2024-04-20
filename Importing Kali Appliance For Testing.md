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

**Description:** Briefly describe what this step involves.

**Actions:**
1. Open a Browser of Your Choosing
2. Click on the Address Bar and Navigate to https://www.kali.org/get-kali/#kali-platforms
3. Select the Option for "Virtual Machines"

**Screenshots:** 
- 

---

### Step 2: Downloading Kali Linux VirtualBox Appliance

**Description:** Briefly describe what this step involves.

**Actions:**
1. After the Page Loads, Locate the "VirtualBox 64" Box
2. Click The Download Button (Marked in The Screenshot)
3. Wait for the File to Finish Downloading and Extract the Contents to its Own Directory

**Screenshots:** 
- 

---

### Step 3: Importing Kali Linux Appliance Into VirtualBox

**Description:** Briefly describe what this step involves.

**Actions:**
1. Open VirtualBox and Click the Green "Add" Button
2. Locate and Select the File in the Directory with Extracted Contents
3. Click the "Select" Button to Begin the Import

**Screenshots:** 
- 
- 

---

### Step 4: Configuring Kali To Use Host-Only Adapter

**Description:** Briefly describe what this step involves.

**Actions:**
1. Click on the Imported VM to View the VM Summary Page
2. Locate and Click on the "Network" Tab
3. Confiure the VM to Utilize the Created Host-Only Adapter and Hit the "OK" Button to Confirm Settings

**Screenshots:** 
- 
- 

---

### Step 5: Starting The Kali Linux VM

**Description:** Briefly describe what this step involves.

**Actions:**
1. Select The Imported VM to View the VM Summary Page
2. Click the Green "Start" Button
3. A New Window Will Appear Displaying the VM

**Screenshots:** 
- 
- 

**Tips:** 
- To Confirm The VM is Using the Host-Only Adapter, Launch a Terminal and use the 'ifconfig' command. The 'inet' address under the 'eth0' interface should display a 172.16.111.x address.

---

## Troubleshooting

Here are some common issues you might encounter and their solutions:

- **Issue 1:** Description of the issue and solution.
- **Issue 2:** Description of the issue and solution.
- **Issue 3:** Description of the issue and solution.

---

## Conclusion

Congratulations! You have completed all the steps and achieved [describe the goal or outcome]. 

---