<h1>Security-Monitoring</h1>

 

<h2>Description</h2>
As part of my cybersecurity and cloud computing apprenticeship, I implemented a security monitoring system on AWS. This project aimed to detect and alert on critical changes in the AWS environment, including the deletion of S3 buckets, which can indicate a malicious action or a misconfiguration.
<br />


<h2> Utilities Used</h2>

- <b>CloudTrail</b> 
- <b>CloudWatch</b>
- <b>S3 </b>

<h2>Environments Used </h2>

- <b>AWS console</b> 

<h2>Steps walk-through:</h2>


- <b>Enable AWS CloudTrail to track AWS resource activities and changes.</b>

  <b> 1️⃣ Access AWS CloudTrail</b>
  
  .<b> Log in to your AWS Console.</b>
  
  .<b> In the search bar, type CloudTrail and click on it.</b>

  <b>2️⃣ Create a New Trail</b>

  .<b>Click on Create a Trail.</b>
<p align="center">
    Activation of AWS CloudTrail <br/>
    <img src="https://raw.githubusercontent.com/Juniorklb/Security-Monitoring-Project-on-AWS/main/Cloudtrail.PNG" alt="CloudTrail Screenshot" width="80%">
 
     CloudTrail has been enabled to capture logs of all AWS activities.
    
</p>

- <b>Configure a CloudWatch Log Group to store CloudTrail logs.</b>

  <b>1️⃣ Go to CloudWatch → Log Groups.</b>

  <b>2️⃣ Click on Create log group.</b>

  <b>3️⃣ Name the log group: CloudTrailLogs.</b>
  
  <b>4️⃣Set a retention: 1 week.</b>

  <b>5️⃣ Associate the Log Group with CloudTrail logs.</b>
  

  
<p align="center">
    Configuration of Cloudwatch to CloudTrail <br/>
    <img src="https://github.com/Juniorklb/Security-Monitoring-Project-on-AWS/blob/c528256f1efa144520f8f9b5ab1b3e2a45730c8d/CloudtrailCloudwatch.PNG"
     alt="CloudTrail Screenshot" width="80%">
 
- <b>Create a metric filter on CloudWatch to detect S3 bucket deletion.</b>

- <b>Test the solution and verify the alerts are working correctly.</b>

- <b>Configure a CloudWatch Log Group to store CloudTrail logs</b>
<p align="center">
<br />
<br />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
