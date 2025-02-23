# AWS Security Monitoring & Automation

## 🚀 Project Overview
This project implements a **security monitoring system** in AWS that detects multiple failed login attempts and automatically disables the compromised IAM user. It enhances security by preventing unauthorized access in real time.

## 🔹 AWS Services Used
- **AWS CloudTrail** – Tracks user activity and failed login attempts.
- **AWS CloudWatch** – Monitors login failures and triggers alarms.
- **AWS Lambda** – Automates security responses by disabling compromised IAM users.
- **AWS IAM** – Manages user access and security policies.

## 🔍 How It Works
1. **CloudTrail** logs all AWS login attempts.
2. **CloudWatch** monitors failed login attempts and triggers an alarm.
3. **Lambda Function** is triggered to disable the IAM user if multiple failed attempts are detected.
4. The compromised user's login profile and MFA are deactivated to prevent unauthorized access.

## 🛠️ Setup Guide
### **Step 1: Enable CloudTrail**
1. Go to **AWS Console → CloudTrail → Create Trail**.
2. Name the trail and enable **Management Events**.
3. Save the trail.

### **Step 2: Create a CloudWatch Alarm**
1. Go to **AWS Console → CloudWatch → Alarms → Create Alarm**.
2. Select **CloudTrail as data source**.
3. Choose **Failed Console Login Attempts** as the metric.
4. Set threshold to **3 failed logins in 5 minutes**.
5. Choose **SNS topic** for notifications (optional).
6. Save the alarm.

### **Step 3: Create a Lambda Function**
1. Go to **AWS Console → Lambda → Create Function**.
2. Choose **Python 3.9**, name it `DisableUserOnFailedLogins`.
3. Add the following code:

```python
import json
import boto3

iam = boto3.client('iam')

def lambda_handler(event, context):
    print("Event:", json.dumps(event))
    username = event.get("detail", {}).get("userIdentity", {}).get("userName")
    if username:
        try:
            iam.update_login_profile(UserName=username, PasswordResetRequired=True)
            iam.deactivate_mfa_device(UserName=username, SerialNumber="mfa-device-serial")
            print(f"User {username} has been disabled due to multiple failed logins.")
        except Exception as e:
            print(f"Error disabling user {username}: {str(e)}")
    return {"statusCode": 200, "body": json.dumps("Security automation executed successfully")}
```

### **Step 4: Attach IAM Permissions**
1. Go to **AWS IAM → Roles**.
2. Select the role attached to the Lambda function.
3. Attach the following permissions:
   - `iam:UpdateLoginProfile`
   - `iam:DeactivateMFADevice`

### **Step 5: Connect CloudWatch Alarm to Lambda**
1. Edit the CloudWatch Alarm.
2. Select **Send to an AWS Lambda function**.
3. Choose the **DisableUserOnFailedLogins** function.
4. Save changes.

### **Step 6: Test Your Setup**
1. Try logging in with an **IAM user** using the **wrong password multiple times**.
2. Check **CloudWatch Logs** for Lambda execution.
3. Verify the IAM user’s **login profile is disabled**.

## 📌 Results & Future Improvements
✅ **Successfully detects failed logins and disables IAM users automatically**. 
🚀 **Future Improvements:** Implement SNS notifications and integrate AWS Security Hub.

## 📎 Junior Kalomba
Developed as part of my AWS Security and Cloud Engineering practice.

---
**🔗 Feel free to contribute or suggest improvements!** 


<a href="https://linkedin.com/in/junior-kalomba-10002a18a" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="junior-kalomba-10002a18a" height="30" width="40" /></a>
