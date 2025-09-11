# HomeLab

## Objectives

This peoject is to set up a homelab and document my different projects I do. I will be expanding my knowledge in system administration, threat detection, and using SIEM tools. 

## Skills Learned

- How to setup VM's and properly configurate them for how I am using them.
- How to use offensive security tools.
- How to monitor malicious activity using Splunk, Sysmon, and event logs.
- Sandboxed the VMs from host network to give myself a safe testing environment.

## Tools Used

- VirtualBox (Windows and Kali Linux)
- Splunk
- Sysmon
- Offensive Security (Nmap and Metasploit)
- Endpoint Security (Microsoft Defender)

## Steps

### Step 1

I installed a Windows 10 VM and a Kali Linux VM. 

### Step 2

I configured my network settings to Internal in both my Windows and Kali because I will be using tools that are malicious so I will be sandboxing these VMs from my host network.

### Step 3

Next, I downloaded and installed Splunk on my Windows 10 VM. 

### Step 4

Next, I downloaded Sysmon and an olaf configuration on my Windows 10 VM.

### Step 5

I then used Windows Powershell with admin privileges to install Sysmon with the configuration.

### Step 6

After using Nmap to run a scan on my Windows VM, I noticed that the RDP port is open, port 3389.

### Step 7

Now I will create a telemetry that I will be able to view on my Windows VM using my monitoring tools.

### Step 8

Now that I have configured the port with our malware, I will open up a handler to listen in on that port by using metasploit.

### Step 9

Next I set up a http server on my Kali VM so the Windows VM can download the malware. I used python.

### Step 10

After configuring my Windows Security settings to be able to download this file, I went downloaded the file.

### Step 11

Lastly, I was able to go on Splunk and look at all the commands that were being executed on the Kali Linux and the file that I created. 

