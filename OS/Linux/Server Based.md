## Get distro information
```bash
cat /etc/*-release
```

## Change PHP version in Linux and apashe2
```bash
sudo a2dismod php7.4
sudo a2enmod php7.4
sudo service apache2 restart
sudo update-alternatives --config php
sudo update-alternatives --config phar
sudo update-alternatives --config phar.phar
sudo service apache2 restart
```

## Install php extensions
```bash
sudo apt-get install php7.4-gd php7.4-xml php7.4-imagick php7.4-zip php7.4-intl php7.4-mysqli php7.4-mbstring php7.4-curl
```

## Enable cron
```bash
sudo systemctl enable cron
```

## Generate #SSH key on legacy linux
```bash
ssh-keygen -t ecdsa -b 521 -C "your_email@example.com"
```

## Show access logs
```bash
cat /var/log/auth.log
```

