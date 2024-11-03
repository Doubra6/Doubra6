# Windows-Server-With-Active-Directory and Powershell Automation-

![Active Directory, Server, with Powershell]![image](https://github.com/Knighthawk76/Windows-Server-With-Active-Directory-/assets/152114740/f095eed7-f6f8-40c3-b09d-f71763eee261)


## Introduction

In this project, I build a full blown active directory lab on a windows server from my desktop computer using Oracle Virtual Box. Upon creating the server and active directory infastructure, I leverage powershell to execute a script that automates the onboarding of  1000 users. This greatly decreases time and effort as well as the potential of human errors. The goal is to gain a better understanding of Active Directory operations, the power of Powershell, and to gain a better understanding of Windows server administration.     

## Resources and Tools

For this project I will be leveraging my home computer, Windows Server 2019 which will be my domain controller, a Windows 10 virtual machine as a client, and Oracle Virtual Box as the tool to architect my Virtual Desktop Infrastructure. I leveraged powershell to do some of the heavy lifting like creating 1000 users which might simulate the scale of a small organization.  The script is also scalable if there were a need to add and create more users, and it was a strong ally for saving me time. The domain controller will house our active directory, and will be configured with two network interface cards(NIC). One will be used for outside internet and the other to the private networks (virtual Box).     
)

![Architecture Diagram](https://github.com/Knighthawk76/Windows-Server-With-Active-Directory-/assets/152114740/da615c01-fb6d-496c-8b0c-d27049fce35d
![Architecture Diagram](https://github.com/Knighthawk76/Windows-Server-With-Active-Directory-/assets/152114740/ca80f909-7858-4ce7-ba29-2f8dedc05ac6)
![Architecture Diagram](https://github.com/Knighthawk76/Windows-Server-With-Active-Directory-/assets/152114740/f54626eb-0cee-415f-8a58-a497c9ee6e18)




## Task 1 Configuring the Domain Controller
I installed Oracle Virtual Box, Windows server ISO, and Windows 10 ISO. Used the Server ISO as the image for the Domain controller Image. Adjusted settings in oracle to allocate 3 processors and 2gb of memory. This may not be enough for some workloads, but it was sufficient for my project. Successful installation and configurations resulted in a base server infrastructure. 

![Architecture Diagram](https://github.com/Knighthawk76/Windows-Server-With-Active-Directory-/assets/152114740/e29e4139-d3a0-4150-af41-dae2327b6c61)

![Architecture Diagram](https://github.com/Knighthawk76/Windows-Server-With-Active-Directory-/assets/152114740/92965273-e3d1-43d1-ac6c-1f1a7c80760a)

## Task 2 more configuring 

The next thing is to add the funcionality I needed for my server. I proceeded with assigning IP adressing for the internal network. the external network gets addressing from my home router. Next I name the server, and add Active Directory, and configure Nat and routing so all the clients on my private networks can connect to the internet. I also setup a DHCP on the domain controller so my clients can automatically recieve an IP address.


![Architecture Diagram](https://github.com/Knighthawk76/Windows-Server-With-Active-Directory-/assets/152114740/f794ce1d-78b9-488c-88dd-3dd36283b285)

![Architecture Diagram](https://github.com/Knighthawk76/Windows-Server-With-Active-Directory-/assets/152114740/7d8c191b-c579-4e5a-a2bf-afcbc2f2c48c)

![Architecture Diagram](https://github.com/Knighthawk76/Windows-Server-With-Active-Directory-/assets/152114740/6114d2eb-7e82-49a4-9ad9-2bd4641f679a)

![Architecture Diagram](https://github.com/Knighthawk76/Windows-Server-With-Active-Directory-/assets/152114740/8d7418aa-7272-47fb-a003-3457ab6edffc)


## Task 3 Powershell script on the Domain Controller

Here I am using a script that generates users and groups them into user by username. Leveraging the script created the users OU and assigned a username for all onboarded candidates.  



![Architecture Diagram](https://github.com/Knighthawk76/Windows-Server-With-Active-Directory-/assets/152114740/fea5d7fb-4e26-494b-b6a3-a52a50a78e2e)

![Architecture Diagram](https://github.com/Knighthawk76/Windows-Server-With-Active-Directory-/assets/152114740/b5a2d262-17ea-482e-8515-c264f7feb60d)

![Architecture Diagram](https://github.com/Knighthawk76/Windows-Server-With-Active-Directory-/assets/152114740/e3d70a14-4fd7-4593-8600-324911fb5691)

![Architecture Diagram](https://github.com/Knighthawk76/Windows-Server-With-Active-Directory-/assets/152114740/e5f603ce-1ae7-4190-911a-c3ae98610305)


## Task 4 Install and Configure Windows 10 Client

Last step is creatng the Windows 10 client in Virtual Box. The VM was configured to have 4 processors and 2gb of Memory.  I utilized commandline on the client to run ipconfig to determine that the VM could reach the internet.  We were able to ping with VM which proves that the infrastructure is working.  I was also able to ping the myDomain.com and there was a response which means there is connectivity throught our build.

![Architecture Diagram](https://github.com/Knighthawk76/Windows-Server-With-Active-Directory-/assets/152114740/78cfc74a-52d5-4f9f-ad31-0cb1e8c35d74)


![Architecture Diagram](https://github.com/Knighthawk76/Windows-Server-With-Active-Directory-/assets/152114740/6f24b218-a4e9-416b-9434-0db6d4fa5f93)


![Architecture Diagram](https://github.com/Knighthawk76/Windows-Server-With-Active-Directory-/assets/152114740/d9c6efc8-e8df-47c3-b4ba-6ea511dd67cd)



![Architecture Diagram](https://github.com/Knighthawk76/Windows-Server-With-Active-Directory-/assets/152114740/faa58e69-7638-494e-826d-d2e9e730c499)



 
## Conclusion

In this project, I learned just how detailed the steps are in order to build a portion of organizational infastructure. While my simulation is far from perfect, I am more aware of how much detail goes into this. During this process I got lost quite often and it required me to reach out to people and utilize online information to resolve my questions.  Ultimately I gained a deeper respect for the skills neccessary to be an engineer, how much I still need to learn in terms of securing infrasructure, and the patience needed to achieve the goal. As a result of this project I have more skill with security configurations, windows server, Active Directory, and Powershell. I am more appreciative of the skills in automation and script building. I gained knowledge on how to deploy VDI with Virtual Box, and got more practice with virtual machines. This project makes me more well rounded in terms of building in the cloud and helped me to gain more skill in hybrid models of deployment.     
