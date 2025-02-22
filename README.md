# AWS Security Monitoring Project

## 🎯Overview
This project demonstrates how to monitor and enhance cloud security using AWS services. It helps detect unauthorized access, security threats, and misconfigurations while automating incident responses.

## 📜Features
- **Log Monitoring**: Tracks AWS API activity with CloudTrail.
- **Threat Detection**: Uses GuardDuty to identify security threats.
- **Automated Alerts**: Sends notifications via SNS when suspicious activity is detected.
- **Security Compliance**: Uses Security Hub to assess security posture.
- **Incident Response Automation**: Uses AWS Lambda to take action when threats are found.

## AWS Services Used
- AWS CloudTrail
- AWS GuardDuty
- AWS Security Hub
- AWS CloudWatch
- AWS IAM (Identity & Access Management)
- AWS Lambda
- AWS SNS (Simple Notification Service)
- AWS Config

## Setup Instructions
1. **Enable CloudTrail**
   - Go to AWS CloudTrail and create a new trail.
   - Store logs in an S3 bucket with encryption enabled.

2. **Activate GuardDuty**
   - Navigate to AWS GuardDuty and enable threat detection.
   - Set up findings to be sent to Security Hub.

3. **Configure CloudWatch Alarms**
   - Create CloudWatch log groups for security-related logs.
   - Set up alarms for unusual API activity.

4. **Set Up Security Hub**
   - Enable Security Hub and integrate it with GuardDuty and AWS Config.

5. **Automate Incident Response with Lambda**
   - Create an AWS Lambda function to disable compromised IAM users.
   - Trigger the function based on CloudWatch events.

6. **Set Up Alerts with SNS**
   - Configure an SNS topic to send email/SMS notifications when threats are detected.

## Testing the Security Monitoring System
- Simulate unauthorized access attempts.
- Perform privilege escalation attempts.
- Verify that alerts and automated responses are working.

## Future Enhancements
- Add AWS WAF (Web Application Firewall) for additional protection.
- Implement machine learning-based anomaly detection.
- Store security logs in AWS OpenSearch for advanced analysis.

## Repository Structure
```
aws-security-monitoring/
│── README.md  # Project documentation
│── setup/     # CloudFormation or Terraform scripts (if applicable)
│── lambda/    # AWS Lambda functions
│── logs/      # Sample security logs
│── scripts/   # Python/Bash scripts for security automation
└── reports/   # Security reports and dashboards
```

## Author
[Junior Kalomba]- Aspiring Cloud Security Engineer

---

## Contact
<a href="https://www.linkedin.com/in/junior-kalomba-10002a18a/"><img src="https://img.shields.io/badge/-LinkedIn-0072b1?&style=for-the-badge&logo=linkedin&logoColor=white" /></a>

---
Feel free to contribute or suggest improvements!
