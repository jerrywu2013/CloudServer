##Installing Varnish on ubuntu 14.04
```
sudo apt-get install varnish apache2
```
####Find the section begin with "Alternative 2, Configuration with VCL" Make sure it's uncommented and update the port:
```
sudo nano /etc/default/varnish
DAEMON_OPTS="-a :6081 \
             -T localhost:6082 \
             -f /etc/varnish/default.vcl \
             -S /etc/varnish/secret \
             -s malloc,256m
             -t 300"
```
####change Listen 80 to Listen 8080
```
sudo nano /etc/apache2/ports.conf
```
####change VirtualHost 80 to VirtualHost 8080
```
sudo nano /etc/apache2/sites-enabled/000-default.conf
```
####restart Varnish and Apache 
```
sudo service apache2 restart
sudo service varnish restart
varnishstat
```
