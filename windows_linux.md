Getting set up with Linux on Windows
==============================

These notes will provide links and information on how to set up Linux on a Windows system and how to get Atom installed.

# Table of Contents
1. [Enabling Windows Subsystem for Linux](#enabling-windows-subsystem-for-linux)
2. []()     
3. [Sources](#sources)

# Enabling Windows Subsystem for Linux

**Step 1:**    
Open the `PowerShell` as an Administrator and enter the following:   
`dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart`   

**Step 2:**   
At this point, I am assuming your system can work with Linux. To make sure, for x86 systems, the Version should be 1903 or higher, and the Build should be 18362 or higher.

If this is not the case, you can upgrade Windows.

**Step 3:**    
Here, we need to enable the Virtual Machine feature. Again, with the `PowerShell` in Administrator, type the following:     
`dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart`     

You may get an error message around here saying that the Virtual Machine Platform needs to be enabled. To do this, in the Windows search bar type `Turn windows features on or off`. With this done, you should see the following:    

![alt text](Images/TurnWindowsFeatures.PNG)     

Make sure the `Virtual Machine Platform` is enabled and press `OK`. Now run the previous command again.     

**Step 4:**    
Back to the `PowerShell`, and type in: `wsl --set-default-version 2`     

**Step 5:**     
Open the [Microsoft Store](https://aka.ms/wslstore). Here, select the disto you wish to have.   

Once installed, you will be asked to provide a username and password.

# Installing Atom for Linux    

Notes for this section:  
- https://medium.com/@rhdzmota/python-development-on-the-windows-subsystem-for-linux-wsl-17a0fa1839d     

- Instead of vim, use nano:    
https://linuxize.com/post/how-to-create-bash-aliases/    

- To add info to bashrc file, can use the following:     
`echo export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-amd64 >> ${HOME}/.bashrc`     
But really using nano is easiet, maybe just detail that

# Sources
[1] https://docs.microsoft.com/en-us/windows/wsl/install-manual
