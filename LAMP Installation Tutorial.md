#Digitalocean LAMP Installation Tutorial

##Step One—Install Apache
```
sudo apt-get update
sudo apt-get install apache2
```
##Step Two—Install MySQL
```
sudo apt-get install mysql-server libapache2-mod-auth-mysql php5-mysql
sudo mysql_install_db
```
```
By default, a MySQL installation has an anonymous user, allowing anyone
to log into MySQL without having to have a user account created for
them.  This is intended only for testing, and to make the installation
go a bit smoother.  You should remove them before moving into a
production environment.

Remove anonymous users? [Y/n] y                                            
 ... Success!

Normally, root should only be allowed to connect from 'localhost'.  This
ensures that someone cannot guess at the root password from the network.

Disallow root login remotely? [Y/n] y
... Success!

By default, MySQL comes with a database named 'test' that anyone can
access.  This is also intended only for testing, and should be removed
before moving into a production environment.

Remove test database and access to it? [Y/n] y
 - Dropping test database...
 ... Success!
 - Removing privileges on test database...
 ... Success!

Reloading the privilege tables will ensure that all changes made so far
will take effect immediately.

Reload privilege tables now? [Y/n] y
 ... Success!

Cleaning up...
```

##Step Three—Install PHP
```
sudo apt-get install php5 libapache2-mod-php5 php5-mcrypt
sudo nano /etc/apache2/mods-enabled/dir.conf
```
```
<IfModule mod_dir.c>

          DirectoryIndex index.php index.html index.cgi index.pl index.php index.xhtml index.htm

</IfModule>
```

##Install phpMyAdmin
```
sudo apt-get update
sudo apt-get install phpmyadmin
```

##Restart apache

```
nano /etc/apache2/apache2.conf
```

```
ServerName localhost
# phpMyAdmin Configuration
Include /etc/phpmyadmin/apache.conf
```

```
sudo service apache2 restart
```

##Change www directory
```
vi /etc/apache2/sites-enabled/000-default.conf
```
##Change SSH Port
```
cd /etc/ssh
vi ssh_config
vi sshd_config
```
prot 22 → port xxxxx
```
service ssh restart
```

##Change phpmyadmin URL
```
vim /etc/phpmyadmin/apache.conf
Alias /phpmyadmin /usr/share/phpmyadmin
Alias /rename /usr/share/phpmyadmin
```

#Fail2Ban
```
sudo apt-get install fail2ban
cp jail.conf jail.local
fail2ban-client status
sudo service fail2ban start
```
#PermitRootLogin setting
```
vim /etc/ssh/sshd_config 
PermitRootLogin no
sudo adduser xxx sudo
sudo i
sudo passwd root
```
#UFW
```
sudo apt-get ufw
sudo ufw default deny 
sudo ufw status
sudo ufw enable
sudo ufw allow ssh  
sudo ufw allow in 8080 
sudo ufw status numbered
sudo ufw delete rulenumber
sudo ufw deny out 4662  
```
