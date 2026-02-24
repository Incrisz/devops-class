# devops-class

devops cmds used for setup 

# Activate our configuration file for our project
sudo ln -s /etc/nginx/sites-available/henry.conf /etc/nginx/sites-enabled/


# ssl cert generation 
sudo apt update
sudo apt install certbot python3-certbot-nginx

sudo certbot --nginx -d henry.bmp.com.ng