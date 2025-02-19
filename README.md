<h1>Security-Monitoring</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
As part of my cybersecurity and cloud computing apprenticeship, I implemented a security monitoring system on AWS. This project aimed to detect and alert on critical changes in the AWS environment, including the deletion of S3 buckets, which can indicate a malicious action or a misconfiguration.
<br />


<h2> Utilities Used</h2>

- <b>CloudTrail</b> 
- <b>CloudWatch</b>

<h2>Environments Used </h2>

- <b>AWS console</b> 

<h2>Steps walk-through:</h2>


-<b>Enable AWS CloudTrail to track AWS resource activities and changes.</b>

-<b>Configure a CloudWatch Log Group to store CloudTrail logs.</b>

-<b>Create a metric filter on CloudWatch to detect S3 bucket deletion.</b>

-<b>Test the solution and verify the alerts are working correctly.</b>

-<b>Configure a CloudWatch Log Group to store CloudTrail logs</b>
<p align="center">
Launch the utility: <br/>
<img src="https://raw.githubusercontent.com/Juniorklb/your-repo/main/images/cloudtrail.png" width="80%" alt="Disk Sanitization Steps">

<br />
<br />
Select the disk:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
