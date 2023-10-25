Certainly! Here's a step-by-step guide for creating an Ubuntu EC2 instance on the AWS Free Tier:

---

## Creating an Ubuntu EC2 Instance on AWS Free Tier

### Prerequisites:

- An AWS account. If you don’t have one, you can sign up [here](https://aws.amazon.com/).

### Step-by-Step Guide:

1. **Login to AWS Console:**
   - Visit the [AWS Management Console](https://aws.amazon.com/console/).
   - Sign in with your AWS account credentials.

2. **Navigate to EC2 Dashboard:**
   - On the AWS Management Console, find the "Services" dropdown at the top left corner.
   - Click on "EC2" under the "Compute" section.

3. **Launch a New Instance:**
   - In the EC2 Dashboard, click on the "Launch Instance" button.

4. **Choose an Amazon Machine Image (AMI):**
   - You'll be presented with a list of available AMIs.
   - Locate "Ubuntu Server" with the tag "Free Tier Eligible". This usually will be an LTS (Long Term Support) version, such as Ubuntu Server 20.04 LTS.
   - Select it by clicking the "Select" button.

5. **Choose an Instance Type:**
   - You'll be on the "Choose an Instance Type" page.
   - Ensure the "t2.micro" instance is selected, as it is the Free Tier eligible option.
   - Click "Next: Configure Instance Details".

6. **Configure Instance Details:** *(default settings are typically fine)*
   - For most use cases, you can skip this step and click "Next: Add Storage".

7. **Add Storage:**
   - The default size is usually 8GB. Adjust if necessary.
   - Ensure "Delete on Termination" is checked if you want the storage to be deleted automatically when the instance is terminated.
   - Click "Next: Add Tags".

8. **Add Tags:** *(optional but recommended)*
   - Click "Add Tag".
   - Enter "Key" as "Name" and "Value" as a name for your instance, e.g., "Ubuntu-Server".
   - Click "Next: Configure Security Group".

9. **Configure Security Group:**
   - It’s recommended to start with a secure setting. For instance, only allow SSH access from your IP.
   - Select "Create a new security group".
   - Name it something descriptive, e.g., "Ubuntu SSH Access".
   - Add a rule: For "Type", choose "SSH". For "Source", choose "My IP".
   - Click "Review and Launch".

10. **Review Instance and Launch:**
   - Review your settings to ensure everything looks correct.
   - Click the "Launch" button.
   - A prompt will appear asking about key pairs. If you have an existing key pair you'd like to use, select it. Otherwise, create a new key pair, download it, and **keep it safe**. This is essential for accessing your instance.
   - After selecting or creating your key pair, click "Launch Instances".

11. **Access Your New Instance:**
   - Navigate back to the EC2 Dashboard and click on "Instances" in the left sidebar.
   - You should see your new instance launching.
   - Once the "Instance State" is "running", you can SSH into it using the key pair you provided:
     ```
     ssh -i path/to/your-key.pem ubuntu@<Public-IP-of-Instance>
     ```

---

Congratulations! You've successfully launched an Ubuntu EC2 instance on AWS Free Tier. Remember to monitor your usage to avoid unexpected charges, and consider stopping or terminating the instance when not in use.