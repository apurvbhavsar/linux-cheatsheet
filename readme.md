### Update server
`sudo apt update`

### Update and Upgrade server
`sudo apt update && sudo apt -y upgrade`

## Apache Installation

- ## Install Apache2 
  `sudo apt install apache2`

- ## Check Apache status
  `sudo systemctl status apache2`

## Nginx Installation

- ## Install Nginx 
  `sudo apt install nginx`

- ## Check status
  `systemctl status nginx`

- ## Managing the Nginx
  - `sudo systemctl stop nginx` Stop server
  - `sudo systemctl start nginx` Start server
  - `sudo systemctl restart nginx` Restart server
  - `sudo systemctl reload nginx` Reload server
  - `sudo systemctl disable nginx` Disable nginx server
  - `sudo systemctl enable nginx` Enable nginx server

## Install Composer in Ubuntu Server
 - `php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"`

 - `php -r "if (hash_file('sha384', 'composer-setup.php') === '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"`

 - `php composer-setup.php`

 - `php -r "unlink('composer-setup.php');"`

## Mysql Installation on Linux server

### Install MySQL Server
`sudo apt install mysql-server`

### Start Mysql Secure Installation
`sudo mysql_secure_installation`

### Start mysql service and stop MySQL service

`sudo service mysql stop` To stop mysql service

`sudo service mysql start` To start mysql service

### Export mysql database 
`mysqldump -u root -p DatabaseName > filename.sql`

## PHP Installation

## Install PHP

`sudo apt install PHP

### Install Specific version of php
`sudo apt install php8.1`

### Install PHP extension

`sudo apt install php8.1-[extension-name]`

### Install commonly used PHP extensions
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

### Create a PPK file from the Pem file

`puttygen input-file.pem -o output-file.ppk`

### Connect Linux server using SSH

`ssh -i "filepath.pem" username@123.123.123.001`

### Github

## Remove file from all commit

# Use the below command to remove the file from all the commits. 
`git filter-branch --tree-filter 'rm -f filepath' HEAD`
# After that push your changes to git.
`git push origin branch_name --force`

## Useful helper commands in Linux

### Get a List of the Number of lines from each file's
`sudo find . -type f |grep -v "^./public" |grep -v "^./vendor" |grep -v "^./.git" |grep -v "^./node_modules"  |grep -v "^./storage" |grep -v "^./bootstrap" |grep -v "^./composer.lock" |grep -v "^./package-lock.json" |xargs wc -l > list.txt`

### Get the list name of each file's
`find . -type f |grep -v "^./vendor" |xargs wc -l > list.txt`

### Get the service name using the port number. 
`sudo netstat -nlpt |grep 3306`
