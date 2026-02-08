## 1. Update system
sudo apt update -y
sudo apt upgrade

## 2. Install Apache
sudo apt install apache2 -y

## 3. Start Apache
sudo systemctl start apache2
sudo systemctl enable apache2

## 4. For checking Status of Apache
sudo systemctl status apache2

## 5. Install Git
sudo apt install git -y
cd /var/www

##
sudo rm -rf html #if you want then delete html directory as it has default code
ls  #to check html file is delete or not

## 6. Copy your repo to Apache 
sudo git clone LINK-OF-YOUR-GITHUB-REPO

ls # check your repo added or not

## 7. Set Permission
sudo chown -R www-data:www-data /var/www/NAME-OF-YOUR-REPO
sudo chmod -R 755 /var/www/

## 8. Add your repo to apache
sudo nano /etc/apache2/sites-available/000-default.conf  # add repo name to it and then save it using Ctrl+O then exit using Ctrl+X

## 9. Check Configuration
sudo apache2ctl configtest

## 10. Restart you Apache Web-Server
sudo systemctl restart apache2


