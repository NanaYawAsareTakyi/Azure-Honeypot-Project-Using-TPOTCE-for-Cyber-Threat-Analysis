# Azure-Honeypot-Project-Using-TPOTCE-for-Cyber-Threat-Analysis
Deployed a honeypot on Azure Cloud using TPOTCE from GitHub, managed with PuTTY. Configured virtual resources to detect and respond to cyber threats, enhancing cybersecurity measures.

## Objective
This project is aimed at deploying and operating a honeypot on Azure Cloud to enhance cybersecurity measures. This included configuring a virtual machine and network infrastructure for effective monitoring and response to potential cyber threats.

## Skills Learned
#### Cloud Deployment: 
Experience in deploying and configuring honeypots in Azure Cloud environments.

#### Virtualization:
Proficiency in setting up and managing virtual machines to support honeypot operations.

#### Network Configuration: 
Skills in configuring network settings and security measures to facilitate honeypot functionality and data monitoring.

#### Cyber Threat Analysis:
Ability to monitor and analyze honeypot data to detect and understand potential cyber threats and attack techniques.

#### Incident Response:
Knowledge in developing and implementing incident response strategies based on honeypot insights to mitigate security risks.

#### Cybersecurity Awareness: 
Enhanced understanding of cybersecurity principles, particularly related to deception technologies like honeypots, to strengthen overall security posture.

#### Cloud Security Best Practices:
Familiarity with best practices for securing cloud-based environments and applications, ensuring effective protection against cyber threats.

## Tools used
<img src="https://img.shields.io/badge/-Azure-0089D6?&style=for-the-badge&logo=Microsoft%20Azure&logoColor=white" />Cloud platform used for deploying and hosting the honeypot.

<img src="https://img.shields.io/badge/-TPOTCE-333333?&style=for-the-badge" />Honeypot tool sourced from GitHub, utilized for setting up and managing the honeypot environment.
 
<img src="https://img.shields.io/badge/-PuTTY-005C95?&style=for-the-badge&logo=PuTTY&logoColor=white" />SSH client used for remote access and management of the Azure virtual machine hosting the honeypot.
 
## Workflow
To begin with I created and configured a virtual machine which involved creating a resource group, selecting the appropriate region and size of the VM, indicating authentication type, selecting SSH for inbound ports, selecting the compatible image for the honeypot and creating the right sized disk for data storage.

The images below illustrate this step:

![image](https://github.com/NanaYawAsareTakyi/Azure-Honeypot-Project-Using-TPOTCE-for-Cyber-Threat-Analysis/assets/173400465/4185f351-e759-4221-8880-956744751994)




![image](https://github.com/NanaYawAsareTakyi/Azure-Honeypot-Project-Using-TPOTCE-for-Cyber-Threat-Analysis/assets/173400465/1b1e905e-754c-4fea-abbb-6c98cf0748ea)




I configured the network settings to enable bi-directional communication for the honeypot by creating a security rule that opened all ports and permitted unrestricted traffic flow.

The image below illustrates this step:

![image](https://github.com/NanaYawAsareTakyi/Azure-Honeypot-Project-Using-TPOTCE-for-Cyber-Threat-Analysis/assets/173400465/3de854c3-17fe-4b85-98a7-4f77550f82ee)


I utilized PuTTY to establish a connection with the VM by entering its IP address into the PuTTY configuration settings. 

This is illustrated in the image below:

![image](https://github.com/NanaYawAsareTakyi/Azure-Honeypot-Project-Using-TPOTCE-for-Cyber-Threat-Analysis/assets/173400465/205e6743-46fb-4d06-abf9-c9d3392a404d)


In the terminal I provided Putty with the username and password I used to create the VM.

This is illustrated in the image below:


![image](https://github.com/NanaYawAsareTakyi/Azure-Honeypot-Project-Using-TPOTCE-for-Cyber-Threat-Analysis/assets/173400465/a0ed67ff-afd0-4618-bd96-b7b43778458a)


I then run some commands to update and upgrade the package list on the system. To update I used the command “sudo apt update” and to upgrade I used “sudo apt upgrade -y”

The image below illustrates this:

![image](https://github.com/NanaYawAsareTakyi/Azure-Honeypot-Project-Using-TPOTCE-for-Cyber-Threat-Analysis/assets/173400465/7b73b0ae-ab04-4327-8b54-24753d9d3e98)


I then installed git by running “sudo apt install git” in the terminal to allow me download tpotce from github repository. 

The image below illustrates this:

![image](https://github.com/NanaYawAsareTakyi/Azure-Honeypot-Project-Using-TPOTCE-for-Cyber-Threat-Analysis/assets/173400465/3b5f4b44-9b09-4e87-8b00-9d02af61e249)


To download the repository, I ran the command “sudo git clone https://github.com/telekom-security/tpotce”

The image below illustrates this:

![image](https://github.com/NanaYawAsareTakyi/Azure-Honeypot-Project-Using-TPOTCE-for-Cyber-Threat-Analysis/assets/173400465/5f058071-f8ab-408d-a18c-abbb82116f0b)


I then navigated to the correct directory and installed with the “./install.sh --type=user” command.

This is illustrated in the image below:

![image](https://github.com/NanaYawAsareTakyi/Azure-Honeypot-Project-Using-TPOTCE-for-Cyber-Threat-Analysis/assets/173400465/504af162-f084-4920-ab91-f61d3aa8e673)

I configured the installation settings accordingly, entering my username and password to access the t-Pot console directly.

The images below illustrate this step:

![image](https://github.com/NanaYawAsareTakyi/Azure-Honeypot-Project-Using-TPOTCE-for-Cyber-Threat-Analysis/assets/173400465/91179a10-a228-4215-977c-42b49ca2cfb0)


![image](https://github.com/NanaYawAsareTakyi/Azure-Honeypot-Project-Using-TPOTCE-for-Cyber-Threat-Analysis/assets/173400465/39b8fbfe-db62-4b57-9f34-1bc4e0ee6c39)


I used the IP address of the VM in conjunction with my username and password to access the t-Pot web interface.


The image below displays the t-Pot web interface:

![image](https://github.com/NanaYawAsareTakyi/Azure-Honeypot-Project-Using-TPOTCE-for-Cyber-Threat-Analysis/assets/173400465/8b80aec5-6e67-4e46-aedc-0d74a9a39e0f)


I left the honeypot running for a few days to attract as many attackers as possible in a short period of time.


An image of the Attack map below illustrates this:


![image](https://github.com/NanaYawAsareTakyi/Azure-Honeypot-Project-Using-TPOTCE-for-Cyber-Threat-Analysis/assets/173400465/13e0c42b-4648-4642-b244-1fd6755549c6)


## Summary
In this project, I successfully deployed a honeypot on Azure Cloud, establishing a secure virtual environment to attract and analyze malicious activities. Continuous monitoring and analysis of honeypot data provided insights into potential attack vectors, enabling proactive measures to mitigate security risks and strengthen the overall cybersecurity defenses in a cloud-based setting.
