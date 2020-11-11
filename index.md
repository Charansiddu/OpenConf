**OPENCONF INSTALLATION ON UBUNTU**

**INSTALLATION OF OPENCONF**

Run the following commands:

sudo apt-get update

sudo apt-get upgrade

sudo apt-get dist-upgrade

sudo apt install lynx unzip apache2

lynx https://www.openconf.com/download (and download) #or download openconf and send to server with a way such as scp

unzip openconf-7.10.zip

sudo rm /var/www/html/index.html

sudo cp -r openconf/* /var/www/html/ 
sudo apt install php php-mysql php-pear php-xml * php-cgi php-cli

sudo apt install mysql-server

sudo chown -R www-data:www-data/var/www/html/* 
sudo chmod -R g + rwX /var/www/html/*

/etc/init.d/apache2 restart

/etc/init.d/mysql restart

sudo mysql -u root

#on mysql

USE mysql; 

UPDATE user SET plugin = 'mysql_native_password' WHERE User = 'root'; 
FLUSH PRIVILEGES; 

exit;

Sendmail can be installed with sudo apt install sendmail for e-mail operations . If a notification is to be sent to gmail (or hotmail yahoo) or sent from there , mail should be sent using gmail with ssmtp instead of sendmail.

**SENDING MAIL USING GMAIL VIA LINUX SHELL**

The sSMTP program can be used to send e-mails with commands over Linux. So what will this do? I will use this process to e-mail myself when my long process is completed. Another use is to be notified, for example, when a program that needs to run continuously on the server or the server itself stops working.

First of all , we install the sSMTP program.

**sudo apt-get install ssmtp**

Then we open the /etc/ssmtp/ssmtp.conf file with sudo and edit it as follows. You write your gmail address in the first line and your password in the second line. The rest remains as it is.

**AuthUser = ........ @ gmail.com**

**AuthPass = ........**

**FromLineOverride = YES**

**mailhub = smtp.gmail.com: 587**

**UseSTARTTLS = YES**

**step 2:
download php mailler and configure**

Place it in plugin/phpmailler

![image](https://github.com/Charansiddu/OpenConf-Installation-on-Ubuntu/blob/gh-pages/images/image.png)



