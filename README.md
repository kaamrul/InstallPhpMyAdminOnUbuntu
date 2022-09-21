# Install phpMyAdmin On Ubuntu 20.04

## 🛠 Installation and Setup Instructions

1. To update the system first : 
    > `sudo apt update or sudo apt-get update`

2. To install apache2 : 
    > `sudo apt-get install apache2`

3. For moving to the root directory type the command: 
    > `sudo su`

4. Now to install the lamp server type the command: 
    > `apt-get install lamp-server^`
    
5. To install phpmyadmin type the command as: 
    > `apt-get install phpmyadmin –y`

6. One dialog box will appear and select 
    > `the apache2` by pressing spacebar.

7. Now configuring phpmyadmin dialog box will appear and select `yes` after that give the password in my case it’s  `admin or user it will be any name` This password is of `root password`

8. Now, goto the php directory as : 
    > `cd /var/www/html/`

9. If you hit the command as `ls` you can see the index.html file over that directory.

10. To see the php version you are using create info.php using command as : 
    > `nano info.php` 
after that type the code as: 
    > `phpinfo();` 
And press ctrl + o to save and ctrl + x to exit.

11. Now goto the browser and type 
    > `localhost/info.php` 
 you will get the php version.

12. Then in browser go to the 
    > `localhost/phpmyadmin` 
you will have to login now so to create user name and password at first go to 
    > `sudo mysql -p -u root`

13. Create User using command as : 
    > `CREATE USER 'admin'@'%' IDENTIFIED BY 'admin';`  
It means that the user name is `admin` and password is also `admin`

14. Grant Permission using the command as : 
    > `GRANT ALL PRIVILEGES ON . TO 'admin'@'%' WITH GRANT OPTION;`

##### Resource Link : 
    https://www.youtube.com/watch?v=VpygRfO8w9k


## 🛠 Another way to Create User & Grant Permission

### Create user and grant permissions

    > sudo dpkg-reconfigure phpmyadmin

    > sudo ln -s /etc/phpmyadmin/apache.conf /etc/apache2/conf-available/phpmyadmin.conf
    > sudo a2enconf phpmyadmin
    > sudo service apache2 reload

    > sudo apt-get install libapache2-mod-php8.1
    > sudo a2enmod php8.1

    > sudo service apache2 reload

##### Resource Link : 
    https://www.digitalocean.com/community/tutorials/how-to-install-and-secure-phpmyadmin-on-ubuntu-20-04
    https://askubuntu.com/questions/118772/how-to-change-root-password-for-mysql-and-phpmyadmin
