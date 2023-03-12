# CREATE AWS EC2 (Linux VM) AND USE PUTTY TO ACCESS IT

Belows are steps demonstrating how to create EC2 (Virtual Machine-Linux VM) and later access the EC2 using Putty :

**Part 1 : Create Instance in EC2**

Name the EC2 Instance : <br>
<img src="step1.PNG" alt= “” width="500px" height="300px">

Select the image and architect : <br>
<img src="step2.PNG" alt= “” width="500px" height="300px">

Select the instance type and Key Pair (MUST!)<br>
<img src="step3.PNG" alt= “” width="500px" height="300px">

if you select ppk, you could directly use it in Putty <br>
if you select pem, you have to convert it to ppk in putty<br>
<img src="step4.PNG" alt= “” width="500px" height="300px">

Select the security group and allow the ssh traffic <br>
<img src="step5.PNG" alt= “” width="500px" height="300px">

Configure the storage then launch the instance <br>
<img src="step6.PNG" alt= “” width="500px" height="300px">

Try connect to server via the AWS console, click "connect" <br>
<img src="step7.PNG" alt= “” width="500px" height="300px">

Here you could see the username, click "connect" <br>
<img src="step8.PNG" alt= “” width="500px" height="300px">

manage connect to the server : <br>
<img src="step9.PNG" alt= “” width="500px" height="300px">

**Part 2 : Connect To EC2 Instance Using Putty**

Install putty and puttygen from : <br>
https://www.puttygen.com/ <br>

if your key is pem, launch puttygen to convert the pem to ppk: <br>
Click Conversions from the Toolbar, and Import Key <br>
Navigate to your .pem key in the file browser and open it <br>
Select SSH-1 (RSA) from the Parameters box <br>
Click Save private key and save the .ppk file somewhere on your file system <br>
<img src="step15.PNG" alt= “” width="500px" height="300px">

Open putty, key in the IP address (Public IP address or DNS Name) :<br>
<img src="step12.PNG" alt= “” width="500px" height="300px">

Go to Connection>Auth>broswse the ppk key that you created : <br>
<img src="step13.PNG" alt= “” width="500px" height="300px">

Navigate back to session, save the session before connecting! : <br>
<img src="step14.PNG" alt= “” width="500px" height="300px">

After connecting to the server, it would prompted to ask for username: <br>
you may refer to the documentation below for default username: <br>
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/TroubleshootingInstancesConnecting.html

Hope it helps you...
