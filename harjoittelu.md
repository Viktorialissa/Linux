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

### Tietokanta

```
sudo apt-get install postgresql
sudo systemctl start postgresql
sudo -u postgres createdb alisa
sudo -u postgres createuser alisa
```

### Djano

>asennus

```
sudo apt-get update
sudo apt-get install virtualenv python3-pip
mkdir django
cd django
virtualenv -p python3 --system-site-packages env/
source env/bin/activate
which pip
micro requirements.txt
	micron sisään kirjoita: django
pip install -r requirements.t
```
>Versio/admin

```
django-admin --version
which django-admin
```
>Projektin luonti

```
django-admin startproject alisaco
cd alisaco
ls
./manage.py runserver #NOT FOR PRODUCTION
./manage.py makemigrations
./manage.py migrate
```
>superuser ja appi

```
./manage.py createsuperuser
./manage.py appi
micro alisaco/settings.py
micro bms/models.py
```
>models.py sisään
```
# Create your models here.
class Haloo(models.Model):
    name = models.CharField(max_length=200)
```
```
./manage.py makemigrations
./manage.py migrate
```
```
micro haloo/admin.py

from django.contrib import admin
from . import models

# Register your models here.
admin.site.register(models.Haloo)
```
>envistä pois
```
deactivate
```

### Tuotantoasennus

```
mkdir -p publicwsgi/alisaco/static
echo "Jaaha." |tee publicwsgi/alisaco/static/index.html
sudoedit /etc/apache2/sites-available/alisaco.conf
```
> alisaco.conf-tiedostoon hakemistopolku
```
<VirtualHost *:80>
        Alias /static/ /home/alisa/publicwsgi/alisaco/static/
        <Directory /home/alisa/publicwsgi/alisaco/static/>
                Require all granted
        </Directory>
</VirtualHost>
```
>Käyttöön ottaminen

```
sudo a2ensite alisaco.conf
sudo a2dissite frontpage.conf
ls /etc/apache2/sites-enabled
/sbin/apache2ctl configtest
sudo systemctl restart apache2
```

```
sudo apt-get update
sudo apt-get -y install virtualenv
cd
cd publicwsgi/
virtualenv -p python3 --system-site-packages env
source env/bin/activate
which pip
micro requirements.txt
pip install -r requirements.txt
django-admin --version
deactivate
rm -r alisaco/
ls
source env/bin/activate
django-admin startproject alisaco
sudoedit /etc/apache2/sites-available/alisaco.conf
sudo apt-get -y install libapache2-mod-wsgi-py3
/sbin/apache2ctl configtest
sudo systemctl restart apache2
curl -s localhost|grep title
curl -sI localhost|grep Server
cd
cd publicwsgi/alisaco/
micro alisaco/settings.py 
touch alisaco/wsgi.py 
curl -s localhost|grep title
micro alisaco/settings.py 
./manage.py collectstatic
```
