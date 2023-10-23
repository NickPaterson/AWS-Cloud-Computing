# EC2-Tutorial-
## Tutorial: Setting Up an EC2 Instance for Hosting a Web Server

### Contents
1.  [Introduction](#1introduction)
2.  [Account Setup](#2-account-setup)
3.  [Create an EC2 Instance](#3-create-an-ec2-instance)
4.  [Connect to Your Instance](#4-connect-to-your-instance)
5.  [Set Up a Web Server using Apache](#5-set-up-a-web-server-using-apache)
6.  [Dynamic Domain Name Service (DDNS)](#6-dynamic-domain-name-service-ddns)
7.  [Installing HTTPS](#7-installing-https)
8.  [Connecting to Your VM via SSH on Visual Studio Code (VSC)](#8-connecting-to-your-vm-via-ssh-on-visual-studio-code-vsc)





### 1. introduction

Amazon Elastic Compute Cloud (EC2) is a powerful service that allows you to deploy virtual servers in the cloud, making it an ideal choice for hosting web servers. Whether you're running a small personal website or managing a large-scale application, EC2 provides the flexibility and scalability to meet your hosting needs.

In this guide, we will walk you through the essential steps of setting up an EC2 instance to host a web server. By the end of this tutorial, you'll have a functional web server ready to serve your content to the world. We'll cover key concepts such as account setup, instance creation, security group configuration, and the installation of a web server software, like Apache.

So, whether you're a seasoned developer or just beginning your journey in web hosting, this guide will equip you with the foundational knowledge to get your web server up and running on an EC2 instance in no time. 





### 2. Account Setup

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/1d748bb1-e898-45de-88d3-ec6192be9c11)

+ Go to [https://aws.amazon.com/](https://aws.amazon.com/).
+ Click on the “Create an AWS Account” or “Get Started for Free” Button.
+ Input your email and choose an account name.
+ Go to your emails and find the email to verify your account.

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/f8d96357-2430-4e9b-a488-2045e0186859)

+ Create a root password and click continue.
+ Input your contact information (Full name, phone number and address).  Check the terms and conditions, then click continue.
+ You will need to input a credit or debit card, which will temporarily hold up to  $1 USD as a pending transaction. You will be able to access AWS Free tier products for 12 months.
+ To verify your phone number, choose how to receive the code, by text message or my voice call, input your phone number, then type the security check to send the code.
+ Input the code you received then click continue.
+ Choose the Basic Support – Free option. Click Complete Sign Up button.

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/3c75b2be-ec10-45d1-99dd-b0814d6f7fd7)





### 3. Create an EC2 Instance

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/3b8f5f4e-63c8-423b-936f-769df2f9e681)

+ Once you log into your account, the console home page will be displayed, if the EC2 doesn’t show in you recently visited click on view all services. 

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/8a115217-4e7d-4399-92bd-ec0fd02c6b5f)

+ Under the Compute category, choose EC2.
+ This will load your EC2 Dashboard.

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/e7d2f44d-e059-46b7-abdd-5854abfac103)

+ In the EC2 Dashboard, click on the Launch instance button.
+ Input a name for you instance,

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/21d378e3-106a-412c-b029-46badce56148)

+ Under the Application and OS Image section, choose Ubuntu operating system.
+ Amazon Machine Image (AMI) choose the Ubuntu Server 22.04 LTS (free tier eligible).
+ The architecture choose the 64-bit (x86).

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/dbe17fd8-f737-4a24-b6eb-f4e88cd15a10)

+ Choose the t2.micro instance type.

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/4abe63a3-ee11-4928-bfab-b201461afe0c)

+ Click on “Create new key pair” hyperlink. 

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/067f00fb-e01e-4069-89d8-e4582881e88e)

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/f0ee138b-f9b6-48a8-b510-84b5d2541ad2)

+ Name your key pair.
+ Choose RSA key pair type.
+	Choose the .pem format.
+	Click on the create key pair button.
+	A file will be downloaded to your computer.
+	Save the file **(DO NOT LOSE OR DELETE THIS FILE)**.
+	Choose the keypair you just created in the drop down menu.

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/14a6df61-2980-4e5d-abd9-e35983a9c25c)

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/179dd156-227e-4fbb-8734-e4aa821a4f47)

+	In the Network Settings, create a security group.
+	Check Allow SSH traffic from Anywhere.
+	Check Allow HTTPS traffic from the internet.
+	Check Allow HTTP traffic from the internet.

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/cc8e4a38-3f54-4ab8-bed3-2a1714c0d8ce)

+ For the storage type in 16 

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/bc973bdd-d583-4077-936c-7e1c0db1c4c8)

+ Leave the Advance and Summary settings as the default settings.
+	Click on the “Launch instance” Button 

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/6f573112-ab3d-4412-8876-7f2790f34328)





### 4. Connect to your instance

You can connect to your instance via AWS Console, for the initial set up, I would recommend connecting via SSH and using the Key Pair created during the instance set up. 

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/14bfce83-58eb-4e08-a4eb-7cd5c2e48e74)

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/bde7ff57-2030-4c47-aea1-318526d86e3b)

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/c4378091-9887-4819-a728-7d685f617c0b)





### 5. Set up a Web Server using Apache

+ Update and uprade all packages

> sudo apt update

> sudo apt upgrade 

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/d24adb0e-87b3-42c4-9a05-2ea78f2a5500)


+ **Installing and configuring Apache**
+ In the instance console, install and configure Apache by inputting the following commands:

> sudo apt install apache2 apache2-utils

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/8914b577-ce34-4f13-b170-8e0dc77058e6)

+ Type Y to continue with the installation.

> sudo systemctl enable apache2

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/6aa15248-66b4-45d7-8c7a-7d34563f05af)

+ Find your public IP address and copy and paste it into a browser address bar.

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/97f8efca-2810-4afd-8c1f-7328908d66b1)

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/d980bf9c-5791-41df-bf1d-39f81008d2b1)

**Congratulations you now have a running web server! **

+ **Ownerships and groups:**

> sudo chown www-data:www-data /var/www/html -R

> sudo usermod -a -G www-data ubuntu

> sudo chown -R ubuntu:www-data /var/www

> sudo chmod 2775 /var/www && find /var/www -type d -exec sudo chmod 2775 {} \; && find /var/www -type f -exec sudo chmod 0664 {} \;

+ **Creating a website and log directories:**

> sudo mkdir /var/www/bookclub

> sudo mkdir /var/log/apache2/bookclub

+ **Set up the virtual configuration file:**

> cd /etc/apache2/sites-available/

+ Copy the default configuration file and edit the new configuration file:

> sudo cp 000-default.conf bookclub.conf

> sudo nano bookclub.conf

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/d0c49edd-9cdc-47c7-b8a3-2952c5508502)

+ Update the document root to the directory we created earlier to /var/www/bookclub 
+ And update the access and error logs to save in the directory we created earlier in /var/log/apache2/bookclub 
+ Save this file by pressing Ctrl + S on the keyboard and Ctrl + X to close the file.

+ Enable the site by activating the virtual host configuration file.
+ Go to the /etc/apache2/site-available directory:

> cd /etc/apache2/sites-available/

+ Run the command to enable the configuration we created and disable the default file:

> sudo a2ensite bookclub.conf

> sudo a2dissite 000-default.conf

+ Restart Apache

> sudo systemctl restart apache2

+ Create an index.html file
  
> cd /var/www/bookclub

> nano index.html

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/79f09a47-07ef-4022-b62f-c2733618b30c)

+ Save (Ctrl + S) and Exit the file (Ctrl + X)

+ Refresh the browser and you should now see the index file you created.

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/af0b78fb-28c8-40ec-a0b9-b4b6aeabb658)




### 6.	Dynamic Doman Name Service (DDNS)
The AWS instance we created has a dynamic IP that is changing regularly, we can use a service such as Duckdns.org to assign a constant web address that is easy to remember.

Go to [https://duckdns.org](https://duckdns.org/).

+ Sign in using your, Twitter, GitHub or Google account.
  
![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/eef83211-5381-4a95-bde1-73960bcdd579)

+ Input a unique web address and click add domain.

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/20c8940f-94bc-4241-a5fa-ef25a9bccb93)
![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/fb66ca34-9a21-4fd5-bfca-1bacb94ad519)

+ Click install on the button in the menu at the top of the page.

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/d5988de2-5ed7-4085-bcb6-77277b6169d0)

+ Choose the linuxcron in the operating system section.
+ Choose your domain you created from the dropdown menu.

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/2c491cc5-5770-4b72-986c-64804eac19f7)

+ Follow the instructions in the linux cron section, ensure linux is running crontab and curl is installed.
+ You may need to adapt and personallised some of the commands:

> cd ~

> mkdir duckdns

> cd duckdns

> nano duck.sh

+ Copy and paste the code from your instructions on Duckdns

```code
echo url="https://www.duckdns.org/update?domains=YOUR_DOMAIN&token=YOUR_TOKEN&ip=" | curl -k -o ~/duckdns/duck.log -K –
```

+ Press Ctrl + S to save and Ctrl X to exit the file.

> chmod 700 duck.sh

> crontab -e 

+ Choose 1 and press enter.

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/f6cf9d63-641e-41cd-84b4-eb0169f75557)

+ Copy and paste the code into the bottom of that file which will run a script to update Duckdns with the new IP address every 5 minutes

```code
*/5 * * * * ~/duckdns/duck.sh >/dev/null 2>&1
```

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/40b46326-ec2f-4ddf-832b-5ccc8c44eb48)

+ Press Ctrl + S to save and Ctrl X to exit the file.
+ Test the script:

> ./duck.sh

> cat duck.log 

+ This should return OK.

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/7a3aaf3c-c5b6-4db3-b184-7c117dc73be5)

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/82d384fd-f142-4deb-a6da-3114e099570e)

**Your new web address should now be working.**




### 7. Installing HTTPS 

> sudo apt update

> sudo apt install snapd

> sudo snap install –classic certbot

> sudo certbot --apache

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/c7e3f360-c6f4-4189-bd54-2776c189f4c8)

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/8685ae26-c7dd-43fd-96cb-8359c3d0c4f6)

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/c990e33f-f392-4d73-b169-552276292987)





### 8.	Connecting to Your VM via SSH on Visual Studio Code (VSC)

+ Install Remote SSH and SSH Editing Configuration from the VSC marketplace.

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/2ecc0700-482b-425b-8335-f53cd7ac464c)

+ Press Ctrl + Shift + P on your keyboard
+ In the search bar, search for ssh
+ Find add new SSH host
+ Choose the .ssh/config file

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/f0683db0-12ce-4bef-a847-3006550b5e2f)

+ Save this file
+ Press Ctrl + Shift + P on your keyboard
+ Find Connect to SSH Host
+ Choose Linux

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/3e3eccfb-f68d-42cd-bb1d-f2923e07f468)

+ Choose Continue 
+ Wait for the connection to connect
+ Click on open folder

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/e99f696e-12bd-4b2d-a549-905540fdf46f)

+ Type /var/www/bookclub/ into the address bar and click OK

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/0647951a-0dc0-4e69-88ec-3df0bc5e163d)

+ You should now be able to see your index.html file you created in the command line

![image](https://github.com/NickPaterson/EC2-Tutorial-/assets/46958743/2b0e29a9-1e78-485c-b4c1-a0f4b19fc888)
