## Setting Up QRadar On-Premise Community Edition

### 1. Download QRadar Community Edition

- Visit [QRadar Community Edition Download Page](https://www.ibm.com/community/101/qradar/ce/).
- Ensure you have an IBM account to proceed with the download.

![Download Page](https://github.com/user-attachments/assets/c07ccdfe-7f65-45a4-a002-0a787364c8af)

### 2. Download the ISO File

- Locate and download the ISO file from the provided link.

![ISO Download](https://github.com/user-attachments/assets/90ffd459-08dc-4917-af04-060831dfb4ac)

### 3. Create a Virtual Machine

- Use the ISO file to create a new virtual machine.
- Check the minimum system requirements before proceeding.

![VM Creation](https://github.com/user-attachments/assets/3eb572d8-ed77-4a77-8d99-18ca02fea764)
![System Requirements](https://github.com/user-attachments/assets/eaa62891-8405-4ff0-aa20-b3f5e1902ab2)
- Ensure you select SATA for your hard drive configuration.

![SATA Configuration](https://github.com/user-attachments/assets/3534429c-f2b8-482c-9533-76af20df7887)

### 4. Install QRadar

- Begin the installation process. RedHat Linux will install first, followed by QRadar.

![Installation Process](https://github.com/user-attachments/assets/aa9437db-76bc-4f1a-aa51-e4311caed2ea)
![Installation Progress](https://github.com/user-attachments/assets/20fae855-0e71-443e-ab51-1d81bfc47f87)
![Further Installation](https://github.com/user-attachments/assets/f8f0702d-2e22-4c83-adf9-d39280fe9870)
![Progress Update](https://github.com/user-attachments/assets/d4dab7b5-3720-4630-b9f8-7b2cd4b71aed)

- Allow the installation to complete without interruption.

![Continuing Installation](https://github.com/user-attachments/assets/d133ecfe-1d8a-489c-b90c-5056bf338546)
![Installation Screen](https://github.com/user-attachments/assets/1694f989-eecd-47cc-b4aa-f12c0fbbf875)
![Final Steps](https://github.com/user-attachments/assets/5627bef8-d055-4a37-bcf4-42429b06d068)
![Almost Done](https://github.com/user-attachments/assets/68631872-4fcf-4077-a7ff-9f58bde4810f)

### 5. Initial Login

- QRadar will prompt for login; use the username `root`.

![Login Screen](https://github.com/user-attachments/assets/77604257-4ec5-421f-9b6b-061125fa3da9)
- Accept the license agreement to proceed.

![License Agreement](https://github.com/user-attachments/assets/979ef299-dad1-4ee0-b84d-5472b28db01b)
![Agreement Confirmation](https://github.com/user-attachments/assets/cc101f73-73c0-43ad-b0fe-c0862cb12026)

### 6. Appliance Setup

- Select "Appliance Install" and then choose "Software Install."

![Software Install](https://github.com/user-attachments/assets/256ad351-c329-40c1-97b3-765e36268bd5)
- Proceed with default settings unless specific changes are required.

![Default Settings](https://github.com/user-attachments/assets/4c96552b-0673-44e7-863f-f220e241580b)

### 7. Network and Credential Setup

- Configure a static IP address for the server.

![Static IP Setup](https://github.com/user-attachments/assets/5a6ac80c-2eb1-4b97-bfe6-0a9def71be9a)
- Set up admin credentials, which will be used for web console access.

![Admin Setup](https://github.com/user-attachments/assets/5f87fcfc-d11c-4bea-94ed-f6d2cedae388)
- Create a strong root password.

![Root Password](https://github.com/user-attachments/assets/3f6c4a6b-72d2-4524-845c-0c6a32dd0220)

### 8. Finalizing Installation

- Allow the installation to continue until complete.

![Installation Continuation](https://github.com/user-attachments/assets/7cf017d2-32db-4bf3-a73b-5ca36185f6d1)
![Final Steps](https://github.com/user-attachments/assets/6f5531ab-388f-4451-9199-3eef53574230)
- Once done, confirm the successful installation.

![Installation Complete](https://github.com/user-attachments/assets/431efef2-1ccf-4eb7-afad-e1b5c1acc274)
![Completion Screen](https://github.com/user-attachments/assets/25818a72-c4b6-4294-8e6b-72b5240172c4)

## 9. Logging Into the Web Console

- Access the QRadar web console via:
  
  `https://<server IP address>`

- Use the credentials set up previously:
  
  **Username:** admin  
  **Password:** [the one you set up earlier]

![Web Console Login](https://github.com/user-attachments/assets/6ddbcdf7-b7f8-4b0c-8509-11d849e172f0)






---
---
## Setting up Qradar On-premise Community Edition

1. Download QRadar Community Edition 

https://www.ibm.com/community/101/qradar/ce/

![image](https://github.com/user-attachments/assets/c07ccdfe-7f65-45a4-a002-0a787364c8af)

Please note that you will need an IBM account to proceed on the download.

2. DOwnload the ISO file

![image](https://github.com/user-attachments/assets/90ffd459-08dc-4917-af04-060831dfb4ac)

3. Create a virtual machine using the ISO and check the minimum requirements

![image](https://github.com/user-attachments/assets/3eb572d8-ed77-4a77-8d99-18ca02fea764)

![image](https://github.com/user-attachments/assets/eaa62891-8405-4ff0-aa20-b3f5e1902ab2)

Please ensure that you are using SATA for your hard drive

![image](https://github.com/user-attachments/assets/3534429c-f2b8-482c-9533-76af20df7887)

4. Proceed with the installation. It will install RedHat Linux first then the Qradar platform.

This will take a while, let it do what is doing 

![image](https://github.com/user-attachments/assets/aa9437db-76bc-4f1a-aa51-e4311caed2ea)

![image](https://github.com/user-attachments/assets/20fae855-0e71-443e-ab51-1d81bfc47f87)

![image](https://github.com/user-attachments/assets/f8f0702d-2e22-4c83-adf9-d39280fe9870)

![image](https://github.com/user-attachments/assets/d4dab7b5-3720-4630-b9f8-7b2cd4b71aed)

![image](https://github.com/user-attachments/assets/d133ecfe-1d8a-489c-b90c-5056bf338546)

![image](https://github.com/user-attachments/assets/1694f989-eecd-47cc-b4aa-f12c0fbbf875)

![image](https://github.com/user-attachments/assets/5627bef8-d055-4a37-bcf4-42429b06d068)

![image](https://github.com/user-attachments/assets/68631872-4fcf-4077-a7ff-9f58bde4810f)

Then it will proceed on installing qradar

![image](https://github.com/user-attachments/assets/5eb7b858-a02b-4ce1-a915-3317aa21d2eb)

![image](https://github.com/user-attachments/assets/a039dcc4-4c84-4357-9484-7cf9dd58c12d)

5. It will require a login, use root

![image](https://github.com/user-attachments/assets/77604257-4ec5-421f-9b6b-061125fa3da9)

accept license agreement

![image](https://github.com/user-attachments/assets/979ef299-dad1-4ee0-b84d-5472b28db01b)

![image](https://github.com/user-attachments/assets/cc101f73-73c0-43ad-b0fe-c0862cb12026)

6. Proceed with the Appliance Install

7. Select Software Install

![image](https://github.com/user-attachments/assets/256ad351-c329-40c1-97b3-765e36268bd5)

you can proceed with the default settings

![image](https://github.com/user-attachments/assets/4c96552b-0673-44e7-863f-f220e241580b)

set up the static IP address for the server

![image](https://github.com/user-attachments/assets/5a6ac80c-2eb1-4b97-bfe6-0a9def71be9a)

set up admin credentials09, this will be used to login to the web console

![image](https://github.com/user-attachments/assets/5f87fcfc-d11c-4bea-94ed-f6d2cedae388)

set root password

![image](https://github.com/user-attachments/assets/3f6c4a6b-72d2-4524-845c-0c6a32dd0220)

installation will continue

![image](https://github.com/user-attachments/assets/7cf017d2-32db-4bf3-a73b-5ca36185f6d1)

![image](https://github.com/user-attachments/assets/6f5531ab-388f-4451-9199-3eef53574230)

completed

![image](https://github.com/user-attachments/assets/431efef2-1ccf-4eb7-afad-e1b5c1acc274)

![image](https://github.com/user-attachments/assets/25818a72-c4b6-4294-8e6b-72b5240172c4)

## Loggin in to web console

https://<server IP address>

username: admin
password: the one that was setup up previously

![image](https://github.com/user-attachments/assets/6ddbcdf7-b7f8-4b0c-8509-11d849e172f0)


