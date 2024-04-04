# Deployed-Web-Application-on-AWS-EC2
This repository contains scripts and configurations used to deploy and manage a web application on Amazon Web Services (AWS) Elastic Compute Cloud (EC2) instances.

Select EC2 from the Services Menu
Select Launch Instance and Create an EC2 Instance. 
Choose appropriate OS. I have used AWS Linux
Create a Key Pair. (This .pem/ppk file will be the specific key whose presence will enable you to login from anywhere)
We have successfully created & launched the instance.
After initializing the EC2 Instance, we will have to connect it to the VM.
For this we have three methods:
 1. We will use the PuTTY to convert .pem file(The key which we downloaded while creating the instance) to .ppk and launch it on our local  System/machine
 2. If we have downloaded the .ppk file then we can directly initialize the VM on our local Machine/System.
 3. We will directly connect to the VM through the AWS platform
 I have used the 3rd method.

install Apache HTTP Server (httpd) on Ubuntu:
------- $ sudo apt-get update && sudo apt-get install -y apache2

Check Apache Service Status:
------- $ sudo systemctl status apache2

Clone the Repository:
------- $ git clone https://github.com/your-username/your-repository.git

Change your current directory to the cloned repository's directory:
------- $ cd your-repository

move all the contents from the folder to “/var/www/html/”
------- $ sudo mv * /var/www/html/
------- $ cd /var/www/html

Edit the Inbound Rules:

check the status of httpd and then enable & start httpd using the following commands:

Check Apache Service Status:
------- $ sudo systemctl status apache2

To start Apache if it's not running, you can use the following command:
------- $ sudo systemctl start apache2

To stop Apache if it's running, you can use the following command:
------- $ sudo systemctl stop apache2


Now open the public ipv4 address allocated to the EC2 instance we created in new tab. We will be able to see the Portfolio Website.

We have Successfully Deployed the Web Application on AWS Cloud!



