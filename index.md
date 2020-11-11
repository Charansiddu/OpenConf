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


**step 2:
download php mailler and configure**

Place it in plugin/phpmailler

![image](https://github.com/Charansiddu/OpenConf-Installation-on-Ubuntu/blob/gh-pages/images/image.png)



