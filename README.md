# Detection Lab

> Please note that this project is ongoing and is meant solely for learning purposes. Your feedback would be greatly appreciated, as I am using this opportunity to learn.

## Objective

To create a controlled environment with a SIEM like Splunk for monitoring, analyzing, and correlating security events, enabling the development of custom rules and improving incident response strategies.

## Initial Setup

We will use Splunk Enterprise for the setup, a widely recognized and trusted SIEM platform known for its robust capabilities in security event monitoring and analysis.

***1. Setting up the server for Splunk installation.***
   
- Choose your preferred operating system and follow the respective guide to spin up a machine:
   - For Windows, refer to the [Windows setup guide.](https://github.com/mmhgwyjs/windows-lab)
   - For Linux, refer to the [Linux setup guide](https://github.com/mmhgwyjs/linux-lab).

***2. Downloading the Splunk installer.***

- Create a Splunk account if you don’t already have one.
- Download the appropriate installer package for your operating system from the official Splunk website: [Splunk Enterprise Downloads](https://www.splunk.com/en_us/download/splunk-enterprise.html).
- For this guide, Red Hat Linux is used as the operating system.

  ![image](https://github.com/user-attachments/assets/90f7b1da-2e75-4353-99be-395348690183)

***3. Installing Splunk Enterprise.***  

- Use the following command to install Splunk:  
  ```
  sudo rpm -i splunk-9.3.1-0b8d769cb912.x86_64.rpm
  ```
   ![image](https://github.com/user-attachments/assets/731e6b69-5931-4649-a47a-b7aa7d1f3bbb)

- Note: The name of the installer will vary depending on the version you've downloaded. Ensure you replace it with the correct file name if needed.

  ![image](https://github.com/user-attachments/assets/1e04c571-374c-4750-a0a3-426c83e367ba)

  ![image](https://github.com/user-attachments/assets/7077c475-aedb-4226-aa94-23ebcc0e53f6)

  > Take note of the Splunk web interface link. By default, it is: `http://127.0.0.1:8000`.
  
***4. Starting Splunk Enterprise.***  

- Change the directory to the Splunk bin folder:  
  ```
  cd /opt/splunk/bin
  ```  
- Run the following command to start Splunk:  
  ```
  sudo ./splunk start
  ```
- During the setup, you will be prompted to set up a username and password. These credentials will be used to log in to the Splunk console.
  
  ![image](https://github.com/user-attachments/assets/0bb6c492-5cc8-4dcf-8129-80eaee098c7e)

  ![image](https://github.com/user-attachments/assets/0e30da16-0e39-47ab-bec8-42da4b25b1e8)

***5. Logging into the Splunk Enterprise Console.***

- From any machine with a browser that can access your Splunk server, open the web interface link noted earlier: `http://127.0.0.1:8000`.

  ![image](https://github.com/user-attachments/assets/168e5521-0831-4c08-bd95-3fbbafe8306a)

- Enter the username and password you set during the setup process to log in to the Splunk console.

  ![image](https://github.com/user-attachments/assets/9cd73fa8-dca5-4a73-865a-7e068b52eb4e)

## Addtional Configurations

### Adding Sample Datasets (Boss of the SOC - BOTS Dataset Version 3) - Optional

- Download the dataset from the following link:  
  [BOTS Dataset Version 3](https://github.com/splunk/botsv3?tab=readme-ov-file)  

- Copy the downloaded file to the directory `/opt/splunk/etc/apps/`:  
  ```  
  cp botsv3_data_set.tgz /opt/splunk/etc/apps/
  ```  

- Extract the dataset:  
  ```  
  sudo tar -xvzf /opt/splunk/etc/apps/botsv3_data_set.tgz
  ```
  ![image](https://github.com/user-attachments/assets/c98147eb-95ef-4347-bb10-cd3286c3b84f)

- Restart the Splunk service to apply the changes:  
  ```  
  sudo /opt/splunk/bin/splunk restart
  ```  
- In the Splunk console, use the following search query to confirm the logs:  
  ```  
  index=botsv3
  ```
  ![image](https://github.com/user-attachments/assets/fcd56231-c696-42ec-acab-285a100183b3)

### Setting up Preferences

- This is optional, but it is recommended to change the time zone to UTC or GMT.

  ![image](https://github.com/user-attachments/assets/3f840738-1a96-4e60-aa55-f85f02c96cee)

  ![image](https://github.com/user-attachments/assets/6ac30c87-01bd-4ec9-9057-50488b110f03)

  ![image](https://github.com/user-attachments/assets/02ae534d-7556-4515-ab88-7397fdde83d5)

#### ***Great job! The detection environment is now set up. Let's move on to the practical exercises listed below.***

## Lab Exercises

| Exercise                                     | Description                                                                                   | Link                                                                                                                       | Status       |
|----------------------------------------------|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|--------------|
| Setting Up a Universal Forwarder to Send Logs to Splunk | Configure a Universal Forwarder on a machine to send logs to Splunk for monitoring and analysis. | [View Exercise](https://github.com/mmhgwyjs/detection-lab/blob/main/Lab%20Exercises/Setting%20Up%20a%20Universal%20Forwarder%20to%20Send%20Logs%20to%20Splunk.md) | In Progress |
| Azure Data Explorer Setup                    | Set up Azure Data Explorer for log collection and query management within your detection environment. | [View Exercise](https://github.com/mmhgwyjs/detection-lab/blob/main/Lab%20Exercises/Azure%20Data%20Explorer%20Setup.md) | In Progress  |
| Boss of the SOC Version 1                  | A cybersecurity simulation where participants act as security analysts in a SOC, investigating security incidents, analyzing logs, and identifying attacks using Splunk. | [View Exercise](https://github.com/mmhgwyjs/detection-lab/blob/main/Lab%20Exercises/BOTSv1.md) | In Progress  |
