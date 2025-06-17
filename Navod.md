# Instalace-wordpress-na-web-server

## instalace nginx

```
sudo apt install nginx -y  
```
```
sudo systemctl enable nginx  
```
```
sudo systemctl start nginx  
```
 

## instalace php 
```
sudo apt install php-fpm php-mysql php-xml php-curl php-gd php-mbstring php-zip php-bcmath php-intl -y  
```
kontrola verze php: 
```
php -v
```

## instalace maria db
```
sudo apt install mariadb-server mariadb-client -y  
```
```
sudo systemctl enable mariadb  
```
```
sudo systemctl start mariadb  
```

### zabezpeceni databaze
```
sudo mysql_secure_installation  
```

Enter current password for root (enter for none):  
   `Pokud jsi ještě nenastavil heslo pro root, jen stiskni Enter.`  

Switch to unix_socket authentication [Y/n]?  
   `Doporučuji: n (ne), pokud chceš přihlašovat přes heslo (např. z phpMyAdminu).`  

Change the root password? [Y/n]  
  `Doporučuji: y`  
  Zadej nové bezpečné heslo pro MySQL uživatele root, pak ho potvrď.  

Remove anonymous users? [Y/n]  
  `Doporučuji: y`  
  Odstraní anonymní účty, které mohou být bezpečnostním rizikem.  

Disallow root login remotely? [Y/n]  
  `Doporučuji: y`  
  Zakáže vzdálené přihlášení jako root, což je bezpečnější.  

Remove test database and access to it? [Y/n]  
  `Doporučuji: y`  
  Odstraní databázi test, která je určena jen pro vývoj.  

Reload privilege tables now? [Y/n]  
  `y`  
Aby se všechny změny projevily okamžitě.  

## stahnuti isp configu
nejdrive se musi zmenit hostname na nejakou domenu napriklad 
```
sudo hostnamectl set-hostname ct102.mojedomena.cz
```
zmena do adresare `/tmp`
```
cd /tmp
```
stahnuti souboru 
```
wget https://www.ispconfig.org/downloads/ISPConfig-3.3.x.tar.gz
```
rozbaleni souboru
```
tar xvfz ISPConfig-3.3.x.tar.gz
```
zmena do adresare `ispconfig3_install/install/`
```
cd ispconfig3_install/install/
```
spusteni instalace
```
sudo php install.php
```
