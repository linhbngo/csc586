---
title: Setup
---

> ## Software Preparation
> We will leverage virtualization to emulate virtual machines for our Linux administration activities. 
> You will need to install the following (free) software on your personal computer (desktop or laptop):
> - [Virtual Box](https://www.virtualbox.org/wiki/Downloads)
> 
> You will need to download the following Linux distro to setup your Linux machines:
> - [Ubuntu 20.04 LTS](https://ubuntu.com/download/server)
{: .prereq}

After finish installing VirtualBox, setup your first Linux virtual machine via the following steps. 

> ## VirtualBox installation on Windows versus Mac
> The screenshots below are taken from a VirtualBox installation on a Mac computer. The graphics will differ
> slightly on a Windows machine, but the major components (buttons) and all contents will be the same. 
{: .callout}

**Step 1:** Click new to create a new virtual machine

<img src="../fig/virtualbox_01.png" alt="Click New to create new virtual machine" style="height:350px">

**Step 2:** Enter the following information
- Name: csc586
- Type: Linux
- Version: Ubuntu (64-bit)

> ## Missing 64-bit option
> If you do not have the 64-bit option, take a look at the following [link to discusstion topic][vb_64-bit]
> for a general solution. The specifics depend on your desktop/laptop brand. 
> It should be OK to use a 32-bit installation for this course, but it is recommended that you try to 
> activate the 64-bit mode. 
{: .callout}

<img src="../fig/virtualbox_02.png" alt="Setup name, OS type, and Linux version" style="height:350px">

**Step 3:** 
- Keep memory at default level, 1024MB. If your PC has more than 4GB of memory, feel free to increase this number. 

<img src="../fig/virtualbox_03.png" alt="Set memory size for the virtual machine" style="height:350px">

**Step 4:**
- Let's create a new virtual hard disk
 
<img src="../fig/virtualbox_04.png" alt="Create a new virtual hard drive" style="height:350px">

**Step 5:**
- Keep VDI as the default hard disk type

<img src="../fig/virtualbox_05.png" alt="Hard disk types" style="height:350px">

**Step 6:**
- Set the hard disk to be dynamically allocated. This means that the size of the hard disk file on your PC will only expand as much as
the actual data you store in your virtual machine. 

<img src="../fig/virtualbox_06.png" alt="Dynamically allocated or fixed size options" style="height:350px">

**Step 7:**
- Set the maximum capacity for the hard disk to 10GB. 

<img src="../fig/virtualbox_07.png" alt="Set hard disk size" style="height:350px">

**Step 8:**
- The virtual machine is now created and available on your virtual machine list. 

<img src="../fig/virtualbox_08.png" alt="New virtual machine created" style="height:350px">

**Step 9:**
- Select your virtual machine, then click the Setting button (Yellow Gear)
- Go to Storage and select the disc under `Controller: IDE`

<img src="../fig/virtualbox_09.png" alt="Virtual machine settings: Storage" style="height:350px">

**Step 10:**
- Click on the Disc icon next to Optical Drive (IDE Secondary Master) and select `Choopse Virtual Optical Disk File ...`
- Navigate to where you downloaded the `Ubuntu 20.04 LTS` image and select that file. 

<img src="../fig/virtualbox_10.png" alt="Select virtual optical disk file" style="height:350px">

**Step 11:**
- The `Ubuntu 20.04 LTS` image file is now loaded. 
- Click `OK` to close the Settings tab. 
- Click `Start` (Green Arrow) to launch the virtual machine. 

<img src="../fig/virtualbox_11.png" alt="Virtual optical disk file is loaded" style="height:350px">

**Step 12:**
- The Linux image file will initiate the installation process. 
- Hit `Enter` to select `English` as the default languange. 
- This is a `CLI` (Command Line Interface), you will only use `arrows` and `Tab` buttons to navigate, `Space` to check boxes, and `Enter` to select. 

<img src="../fig/virtualbox_12.png" alt="Language selection" style="height:350px">

**Step 13:**
- There have been a number of small updates to Ubuntu since 20.04 was released. 
- We will ignore these updates for now. 
- Select `Continue without updating` and hit `Enter`.

<img src="../fig/virtualbox_13.png" alt="Options to update Ubuntu during installation" style="height:350px">

**Step 14:**
- Keep defautl layout and variant of the keyboard to **English (US)**. 
- Hit `Tab` to highlight the **Done** option then hit `Enter`.

<img src="../fig/virtualbox_14.png" alt="Options for keyboard layout and variant" style="height:350px">

**Step 15:**
- Keep the Network setting to default. 
- Navigate to highlight the **Done** option then hit `Enter`.

<img src="../fig/virtualbox_15.png" alt="Network settings" style="height:350px">

**Step 16:**
- Keep the Proxy setting to default.
- Navigate to highlight the **Done** option then hit `Enter`.

<img src="../fig/virtualbox_16.png" alt="Proxy settings" style="height:350px">

**Step 17:**
- This is the link to Ubuntu's archival repository. 
- We do not need to change this. 
- Navigate to highlight the **Done** option then hit `Enter`.

<img src="../fig/virtualbox_17.png" alt="Ubuntu archive link" style="height:350px">

**Step 18:**
- Make sure that you check the box to **Use an entire disk** only. 
- Navigate to highlight the **Done** option then hit `Enter`.

<img src="../fig/virtualbox_18.png" alt="Storage layout setting" style="height:350px">

**Step 19:**
- Keep storage configuration to default. This is a summary of configurations.
- Navigate to highlight the **Done** option then hit `Enter`.

<img src="../fig/virtualbox_19.png" alt="Summary of storage configuration" style="height:350px">

**Step 20:**
- Final confirmation that we will overwrite the selected storage.
- Navigate to highlight the **Continue** option then hit `Enter`.
  
<img src="../fig/virtualbox_20.png" alt="Final storage confirmation" style="height:350px">

**Step 21:**
- Enter your full name. 
- Enter `server-1` for your machine name. We will refer to this name later on during the lessons. 
- Pick a username. Typically it is your first initial + last name. 
- Choose a strong password. While this is only a system for learning purposes, it is important that you practice
the habit of always use strong password. 
  
<img src="../fig/virtualbox_21.png" alt="Name, machine name, username, and password" style="height:350px">

**Step 22:**
- Check the box to **Install OpenSSH server** only.
- Navigate to highlight the **Done** option then hit `Enter`.

<img src="../fig/virtualbox_22.png" alt="Select the installation of OpenSSH server" style="height:350px">

**Step 23:**
- Do not install any additional infrastructure package. 
- Navigate to highlight the **Done** option then hit `Enter`.

<img src="../fig/virtualbox_23.png" alt="Optional packages" style="height:350px">

**Step 24:**
- Wait until the installation and update process is completed. 
- You then can reboot the virtual machine. 
- You may be asked to hit `Enter` one more time when asked to remove installation medium. 

<img src="../fig/virtualbox_24.png" alt="Reboot after installation and update" style="height:350px">

**Step 25:**
- You might need to hit `Enter` one time at this stage of the booting up process. 
  
<img src="../fig/virtualbox_25.png" alt="Booting process seems to pause here" style="height:350px">

**Step 26:**
- You are now able to log in with your username and password specified in **Step 21**.

<img src="../fig/virtualbox_26.png" alt="Click New to create new virtual machine" style="height:350px">

**Step 27:**
- To gracefully shutdown the virtual machine, type `shutdown` and hit `Enter`.
  
<img src="../fig/virtualbox_27.png" alt="Click New to create new virtual machine" style="height:350px">



{% include links.md %}
