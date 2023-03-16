   ### Alku
   
   >micron asennus
   >syslog
    
   ```
      sudo apt-get -y install micro
      sudo lshw -short -sanitize 
     sudo apt-get -y install lshw
     sudo lshw -short -sanitize
     sudo apt-get -y install curl tree python3-py
     ls
     ls /etc/
     ls /var/log/
     var/log/syslog
     sudo cd /var/log/syslog 
     cd var/log/syslog
     cd /var/log/syslog 
     cd /var/log
     sudo cat syslog 
  ```
  
  
  ## Apachen asennus
  
  ```
  sudo apt-get install apache2
  sudo systemctl start apache2
  echo "heippari" | sudo tee /var/www/html/index.html
  cd
  ```
  
  ## Käyttäjän kotisivu localhost/~user
  
  ```
  sudo a2enmod userdir
  systemctl restart apache2
  cd
  pwd 
  mkdir public_html
  cd public_html 
  pwd
  micro index.html
  ```

## Luo uusi käyttäjä

```
sudo adduser user
```

Käyttäjän vaihto `su user`

### kotisivu käyttäjälle

```
whoami
cd
ls
pwd
mkdir public_html
cd public_html/
pwd
micro index.html
```

### HTML5-sivu

```
su user
micro public_html/index.html
```

>HTML käyttäjälle alisa /~alisa
```
<!doctype html>
<html>
<head>
	<title>Alisa Page</title>
	<meta charset="utf-8" />
</head>
<body>
	<h1>Alisa's Test Page</h1>
	<p>Let's test UTF-8 with "päivää"</p>
</body>
</html>
```

### Apachelle etusivu

      sudoedit /etc/apache2/sites-available/frontpage.conf 

>nanossa asetukset:

```
<VirtualHost *:80>
        DocumentRoot /home/alisa/public_sites
        <Directory /home/alisa/public_sites/>
                require all granted
        </Directory>
</VirtualHost>
```
>terminaalissa jatkuu:

```
sudo a2ensite frontpage.conf
sudo a2dissite 000-default.conf
sudo systemctl restart apache2

cd
mkdir public_sites 
micro index.html
sudo systemctl restart apache2

index.html väärässä paikkaa joten siirto okeaan:
mv index.html /home/alisa/public_sites/index.html
```
