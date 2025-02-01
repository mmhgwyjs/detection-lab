## Forward data to Splunk Enterprise Using Universal Forwarder

### 1. Configuring Receiving on a Splunk Enterprise Instance or Cluster

**Step 1:** Open the Splunk Enterprise web interface and log in with your credentials.

**Step 2:** Navigate to **Settings > Data Inputs**.

**Step 3:** Click on **Forwarded Data** to configure receiving.

**Step 4:** Click on **New** to add a new TCP port for data input.

*Refer to the images below for each interface screen during the setup process.*

![Splunk Data Input Configuration](https://github.com/user-attachments/assets/07675823-6b00-4c08-b1cc-316a9a8c7404)

*This image shows the initial Data Inputs screen where you select Forwarded Data.*

![New Data Input](https://github.com/user-attachments/assets/f0f87301-2ab5-42b4-8fac-c3c92df74062)

*Adding a new TCP input for receiving data.*

### 2. Downloading and Installing the Universal Forwarder

**Step 1:** Download the Universal Forwarder from the official Splunk website:

[Splunk Universal Forwarder Download](https://www.splunk.com/en_us/download/universal-forwarder.html)

**Step 2:** Run the installer and follow the prompts:

- Accept the license agreement.
- Choose the installation directory.
- Leave default settings unless specific configurations are required.

*Visual references for each installation step:*

![Universal Forwarder Installation](https://github.com/user-attachments/assets/ab34ae05-b34d-4039-a2d7-7ac75b4023aa)

*Installer initial screen.*

![Installation Progress](https://github.com/user-attachments/assets/248a3e1d-0657-47e2-88a8-eac64b7da402)

*Progress of the installation process.*

### 3. Troubleshooting Common Issues

If you encounter connectivity issues, ensure the necessary ports are open:

- Refer to [this guide](https://linuxconfig.org/redhat-8-open-and-close-ports) for managing firewall settings on RedHat-based systems.

![Firewall Configuration](https://github.com/user-attachments/assets/e403a40d-5897-4165-8c9d-24b428a4db0c)

*Example of opening ports via firewall-cmd.*

### 4. Verifying Data Reception

**Step 1:** Log into Splunk Enterprise.

**Step 2:** Use the Search & Reporting app to verify incoming data:

- Query example: `host="hostname"`

![Search and Reporting](https://github.com/user-attachments/assets/2d1f36db-ade9-4c06-b634-6d90521068d4)

*This image shows how to confirm data is being received correctly.*




---
---
---


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


