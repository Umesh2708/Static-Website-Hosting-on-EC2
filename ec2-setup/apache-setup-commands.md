# 🚀 Apache Deployment Steps (Ubuntu)

1. Update system  
```bash
sudo apt update -y
sudo apt upgrade -y
```

2. Install Apache  
```bash
sudo apt install apache2 -y
```

3. Start Apache  
```bash
sudo systemctl start apache2
sudo systemctl enable apache2
```

4. For checking Status of Apache  
```bash
sudo systemctl status apache2
```

5. Install Git  
```bash
sudo apt install git -y
cd /var/www
```

```bash
sudo rm -rf html   # if you want then delete html directory as it has default code
ls                 # to check html file is deleted or not
```

6. Copy your repo to Apache  
```bash
sudo git clone LINK-OF-YOUR-GITHUB-REPO
ls   # check your repo added or not
```

7. Set Permission  
```bash
sudo chown -R www-data:www-data /var/www/NAME-OF-YOUR-REPO
sudo chmod -R 755 /var/www/
```

8. Add your repo to Apache  
```bash
sudo nano /etc/apache2/sites-available/000-default.conf
# add repo name to it and then save it using Ctrl+O then exit using Ctrl+X
```

9. Check Configuration  
```bash
sudo apache2ctl configtest
```

10. Restart your Apache Web Server  
```bash
sudo systemctl restart apache2
```
