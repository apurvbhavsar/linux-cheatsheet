# Update server
`sudo apt update`

* Update and Upgrade server
`sudo apt update && sudo apt -y upgrade`

* Install Apache2 
`sudo apt install apache2`

* Check apache status
`sudo systemctl status apache2`

* Install MySQL Server
`sudo apt install mysql-server`

* Start Mysql Secure Installation
`sudo mysql_secure_installation`

* Install Php extenstions
`sudo apt install php8.1-mbstring php8.1-intl php8.1-gd php8.1-common php8.1-dom php8.1-curl php8.1-xml php8.1-zip php8.1-zip`

* Get service name using port number. 
`sudo netstat -nlpt |grep 3306`

* Start mysql service and stop mysql service
`sudo service mysql stop`
`sudo service mysql start`

`puttygen input-file.pem -o output-file.ppk`

* Export mysql database 
`mysqldump -u root -p DatabaseName > filename.sql`

* Get List of Number of line from each files
`sudo find . -type f |grep -v "^./public" |grep -v "^./vendor" |grep -v "^./.git" |grep -v "^./node_modules"  |grep -v "^./storage" |grep -v "^./bootstrap" |grep -v "^./composer.lock" |grep -v "^./package-lock.json" |xargs wc -l > list.txt`

* Get list name of each files
`find . -type f |grep -v "^./vendor" |xargs wc -l > list.txt`

* Install Composer in Ubuntu Server
`
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
`
