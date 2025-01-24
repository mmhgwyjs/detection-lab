# Detection Lab

> Please note that this project is ongoing and is meant solely for learning purposes. Your feedback would be greatly appreciated, as I am using this opportunity to learn.

## Objective

To create a controlled environment with a SIEM like Splunk for monitoring, analyzing, and correlating security events, enabling the development of custom rules and improving incident response strategies.

## Initial Setup

We will use Splunk Enterprise for the setup, a widely recognized and trusted SIEM platform known for its robust capabilities in security event monitoring and analysis.

***1. Setting up the server for Splunk installation.***
   
- Choose your preferred operating system and follow the respective guide to spin up a machine:
   - For Windows, refer to the W[indows setup guide.](https://github.com/mmhgwyjs/windows-lab)
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


## forward data to Splunk Enterprise

1. Configure receiving on a Splunk Enterprise instance or cluster.

   ![image](https://github.com/user-attachments/assets/07675823-6b00-4c08-b1cc-316a9a8c7404)

   ![image](https://github.com/user-attachments/assets/f0f87301-2ab5-42b4-8fac-c3c92df74062)

   ![image](https://github.com/user-attachments/assets/2d8d9f05-5506-4b9b-9d7d-56a52028df17)

   ![image](https://github.com/user-attachments/assets/9df6980e-cb34-4a6b-bf8c-6dc23ad66130)

   ![image](https://github.com/user-attachments/assets/72d79660-38a6-418c-a412-c1284e9ba6eb)

2. Download and install the universal forwarder.
   https://www.splunk.com/en_us/download/universal-forwarder.html

   ![image](https://github.com/user-attachments/assets/ab34ae05-b34d-4039-a2d7-7ac75b4023aa)

   ![image](https://github.com/user-attachments/assets/248a3e1d-0657-47e2-88a8-eac64b7da402)

   ![image](https://github.com/user-attachments/assets/50729973-a174-4131-90f9-b8d9cb54389f)
  leave blank

![image](https://github.com/user-attachments/assets/7dbdab06-a243-44a4-8182-01d9425cff1d)

![image](https://github.com/user-attachments/assets/68bdfb1f-aac7-4671-a68b-90fd7640244b)

![image](https://github.com/user-attachments/assets/ad2b4c1f-141a-4a3d-8e5e-b14ed2b889f4)

![image](https://github.com/user-attachments/assets/1482f896-df20-4735-8ec5-65a4ca8ea221)

![image](https://github.com/user-attachments/assets/e8c02a0a-3d61-4dfd-ac57-693a8b73a482)

![image](https://github.com/user-attachments/assets/e460abdd-48eb-4677-b082-197203d4849e)

![image](https://github.com/user-attachments/assets/267f9a39-0596-4b50-94e6-316c0d2f799a)

![image](https://github.com/user-attachments/assets/c4b2c327-5cdf-417d-a815-0bc816ef4541)

![image](https://github.com/user-attachments/assets/806357fb-2810-4f8d-aca9-0fb7bf335b13)

![image](https://github.com/user-attachments/assets/fcccd392-3ddb-4043-9462-bfcbd75b0837)

![image](https://github.com/user-attachments/assets/1b670f21-3043-4451-8615-128d2781aa8e)

troubleshooting
https://linuxconfig.org/redhat-8-open-and-close-ports

![image](https://github.com/user-attachments/assets/e403a40d-5897-4165-8c9d-24b428a4db0c)

![image](https://github.com/user-attachments/assets/7c44b144-7785-43eb-b06e-34bd7a837f2d)

![image](https://github.com/user-attachments/assets/e66e38c7-6b02-4894-b858-81cde6eee5cb)

![image](https://github.com/user-attachments/assets/d5d9f8d0-5993-4ec8-9281-28d976ea00f3)

![image](https://github.com/user-attachments/assets/44ca56de-c891-4fe0-a8fc-dc402c5f6e28)

![image](https://github.com/user-attachments/assets/a62854c1-bbbe-48d7-b0a4-f80e76fba628)


Checking

![image](https://github.com/user-attachments/assets/35a9151f-78f7-47d8-a741-2986f6b89a28)

![image](https://github.com/user-attachments/assets/d9297899-575b-48fa-b080-2d16dc3424f7)

![image](https://github.com/user-attachments/assets/2a7b7f66-9083-4c72-a730-d2f3c8698988)
host="hostname"

![image](https://github.com/user-attachments/assets/2d1f36db-ade9-4c06-b634-6d90521068d4)

