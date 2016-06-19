```
echo "deb http://deb.goaccess.io $(lsb_release -cs) main" | sudo tee -a /etc/apt/sources.list
wget -O - http://deb.goaccess.io/gnugpg.key | sudo apt-key add -
sudo apt-get update
sudo apt-get install goaccess
sudo goaccess -f /var/log/apache/access.log -a
```
