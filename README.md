# Home Lab

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
![HomeLab 1](https://github.com/user-attachments/assets/64c4f341-d078-42ba-840a-07fd75b9d4e1)

### Step 2

I configured my network settings to Internal in both my Windows and Kali because I will be using tools that are malicious so I will be sandboxing these VMs from my host network.
![HomeLab 2](https://github.com/user-attachments/assets/34d03d87-929a-4c53-b3ad-0035d38c82dd)

### Step 3

Next, I downloaded and installed Splunk on my Windows 10 VM. 
![HomeLab 3](https://github.com/user-attachments/assets/0bb26185-b55e-4ad5-bbcc-c9f65ce3a8f2)

### Step 4

Next, I downloaded Sysmon and an olaf configuration on my Windows 10 VM.
![HomeLab 4](https://github.com/user-attachments/assets/bf11ac23-3ccc-4e21-b248-a4e40f688781)

### Step 5

I then used Windows Powershell with admin privileges to install Sysmon with the configuration.
![HomeLab 5](https://github.com/user-attachments/assets/120fade6-91af-43c8-a2f3-64f327b4491b)

### Step 6

After using Nmap to run a scan on my Windows VM, I noticed that the RDP port is open, port 3389.
![HomeLab 6](https://github.com/user-attachments/assets/8c677f0a-b0bd-4a69-b01a-33fdb88ccc78)

### Step 7

Now I will create a telemetry that I will be able to view on my Windows VM using my monitoring tools.
![HomeLab 7](https://github.com/user-attachments/assets/bc251b1d-66bd-48cc-ac29-400b1a8ec38d)

### Step 8

Now that I have configured the port with our malware, I will open up a handler to listen in on that port by using metasploit.
![HomeLab 8](https://github.com/user-attachments/assets/d941ee01-6cdd-4883-a66d-48342b38a12b)
![HomeLab 9](https://github.com/user-attachments/assets/24ab3778-ff9b-4031-9cd4-9db85c0d11a6)
![HomeLab 10](https://github.com/user-attachments/assets/9d2e324e-48a2-485a-ba0e-984f728c5935)

### Step 9

Next I set up a http server on my Kali VM so the Windows VM can download the malware. I used python.
![HomeLab 11](https://github.com/user-attachments/assets/1a97f280-8c31-4628-9b4e-bc225a43d36d)

### Step 10

After configuring my Windows Security settings to be able to download this file, I went downloaded the file.

### Step 11

Lastly, I was able to go on Splunk and look at all the commands that were being executed on the Kali Linux and the file that I created. 

