# Linux_Response_Tool: Ubuntopsy

"In case of emergency insert the USB"

This is a Bash tool that's created for quick use during incident response to a Linux Ubuntu system. It will collect useful volatile and non-volatile data before you shut down the infected device.

You have to save the whole directory Linux_Response_Tool on a USB drive and run the app from it. This app runs on Ubuntu systems and has been tested on Ubuntu 22.10

## Features

- The app will collect the following volatile data: 
Modified Files in the Last 10 Minutes, Running Processes, Process and Ports Information, Routing Table, ARP Information, ifconfig information,  Wireless Interface Info, Open Files Information, Loaded Kernel Modules. 

- Next, it will collect the following non-volatile data: 
System Information, System Log Files, Auth Log Files, Kernel Log Files, Login Information, Login History Information, BIOS information, System Variables, File Systems Information, Memory & Swap Space Storage Information. 

## Getting Started

### Dependencies
The necessary tools to collect the data are located in the "tools" directory. The user will not need to use the local machine's tools. 

### Installing
It is highly recommended to use a USB flash drive that's formatted to ext3 or ext4 and save the directory Linux_Response_Tool on it. 

### Executing the Program

1) Attach the external drive 
2) Open terminal as root user
3) Use terminal to navigate to Linux_Response_Tool on your drive (ex: /media/*username*/*flash drive name*/Linux_Response_Tool)
4) Run application by typing ./response
5) Follow directions on terminal 

## Output
- The collected data will be stored in the "data" directory located in Linux_Response_Tool/data.
- There will also be a summary file that includes the start and end time of collection. 
- Additionally, there will be a file_hashes txt file that contains the hashes (MD5 & SHA256) of all the output files. This is to ensure that no tampering occurs to the output files. You can verify the hashes on a different computer by hashing each output file and verifying that you have the same hashes as what's found in the file_hashes. 
- To view the log files produced in the data directory, launch terminal as a root user and use gedit followed by the log file name. 
(Ex: > gedit /media/*username*/*flash drive name*/Linux_Response_Tool/data/18_auth.log)

## Authors

Ahmed Ali  
https://medium.com/@Akali27
