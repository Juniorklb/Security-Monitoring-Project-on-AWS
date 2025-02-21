<h1>Security-Monitoring with AWS</h1>

 

<h2>Introduction</h2>
This project focuses on implementing a security monitoring system in AWS to detect and alert critical changes within the cloud environment. The system is designed to monitor key security events, such as the deletion of S3 buckets, which could indicate malicious activity or misconfiguration.
<br />


<h2> Prerequisites </h2>

- <b>CloudTrail</b> 
- <b>CloudWatch</b>
- <b>S3 </b>

<h2>Setup requirements </h2>

- [AWS console]("https://ca-central-1.console.aws.amazon.com/console/home?region=ca-central-1")

- <br/><a href="https://ca-central-1.console.aws.amazon.com/console/home?region=ca-central-1"><b>AWS console</b></a>


<h2>Setup instructions</h2>


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

      Amazon CloudWatch is a monitoring and observability service in AWS that helps you collect, analyze, and respond to 
      operational and performance data from your AWS infrastructure, applications, and services. It allows you to monitor 
      resources in real-time, set up alarms, and visualize metrics and logs.

  <b>1️⃣ Go to CloudWatch → Log Groups.</b>

  <b>2️⃣ Click on Create log group.</b>

  <b>3️⃣ Name the log group: CloudTrailLogs.</b>
  
  <b>4️⃣Set retention: 1 week.</b>

  <b>5️⃣ Associate the Log Group with CloudTrail logs.</b>
  

  
<p align="center">
    Configuration of Cloudwatch to CloudTrail <br/>
    <img src="https://github.com/Juniorklb/Security-Monitoring-Project-on-AWS/blob/f410569791caf373629bc99aff2dc085bf404af5/Loggroup.PNG"
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
