 ### Update server
`sudo apt update`

### Update and Upgrade server
`sudo apt update && sudo apt -y upgrade`

### Install Apache2 
`sudo apt install apache2`

### Check apache status
`sudo systemctl status apache2`

## Install Composer in Ubuntu Server
 - `php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"`

 - `php -r "if (hash_file('sha384', 'composer-setup.php') === '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"`

 - `php composer-setup.php`

 - `php -r "unlink('composer-setup.php');"`

## Mysql Installation on linux server

### Install MySQL Server
`sudo apt install mysql-server`

### Start Mysql Secure Installation
`sudo mysql_secure_installation`

### Start mysql service and stop mysql service

`sudo service mysql stop` To stop mysql service

`sudo service mysql start` To start mysql service

### Export mysql database 
`mysqldump -u root -p DatabaseName > filename.sql`

## PHP Installation

## Install PHP

`sudo apt install php`

### Install Specific version of php
`sudo apt install php8.1`

### Install php extenstion

`sudo apt install php8.1-[extension-name]`

### Install commanly used PHP extenstions
`sudo apt install php8.1-mbstring php8.1-intl php8.1-gd php8.1-common php8.1-dom php8.1-curl php8.1-xml php8.1-zip php8.1-zip`

### Check Active PHP Version
`php -v`

### Switch PHP version

- `sudo update-alternatives --set php /usr/bin/php7.4`
- `sudo update-alternatives --set phar /usr/bin/phar7.4`
- `sudo update-alternatives --set phar.phar /usr/bin/phar.phar7.4`

### To uninstall any PHP version just type
`sudo apt remove php8.1`

### To uninstall all the modules for that version
`sudo apt remove php8.1-* `

### Create PPK file from Pem file

`puttygen input-file.pem -o output-file.ppk`

### Connect linux server using SSH

`ssh -i "filepath.pem" username@123.123.123.001`


## Useful helper commands in linux

### Get List of Number of line from each files
`sudo find . -type f |grep -v "^./public" |grep -v "^./vendor" |grep -v "^./.git" |grep -v "^./node_modules"  |grep -v "^./storage" |grep -v "^./bootstrap" |grep -v "^./composer.lock" |grep -v "^./package-lock.json" |xargs wc -l > list.txt`

### Get list name of each files
`find . -type f |grep -v "^./vendor" |xargs wc -l > list.txt`

### Get service name using port number. 
`sudo netstat -nlpt |grep 3306`
