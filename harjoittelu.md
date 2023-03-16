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
