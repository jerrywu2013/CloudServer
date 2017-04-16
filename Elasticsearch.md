### Install Elasticsearch 5.3.0 on ubuntu14.04

##### Add a new user
```
sudo adduser esjerry
sudo visudo
```
```
# User privilege specification
root    ALL=(ALL:ALL) ALL
esjerry ALL=(ALL:ALL) ALL
```
###### Installing elasticsearch
```
sudo apt-get install software-properties-common
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get -y install oracle-java8-installer
curl -L -O https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-5.3.0.tar.gz
tar -xvf elasticsearch-5.3.0.tar.gz
cd elasticsearch-5.3.0
vim config/elasticsearch.yml
```
```
cluster.name: Admin_Cluster
node.name: Jerry DataCenter
node.master: true
node.data: true
transport.host: localhost
transport.tcp.port: 9300
http.port: 9200
network.host: 0.0.0.0
```
```
cd /home/lab/es/elasticsearch-5.3.0/bin
./elasticsearch
```
```
vi /etc/rc.local
su - esjerry -c "/home/jerry/elasticsearch-5.3.0/bin/elasticsearch -d"
```
curl -X GET 'http://IP:9200'

curl -X POST 'http://IP:9200/tutorial/helloworld/1' -d '{ "message": "Hello World!" }'

curl -X GET 'http://IP:9200/tutorial/helloworld/1'
```

```
https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-elasticsearch-on-ubuntu-14-04

http://tecadmin.net/install-elasticsearch-on-linux/

http://javacore.cn/page/146/elasticsearch-233-ubuntu-under-the-installation-configuration-boot.html

https://github.com/rippleblue/Elasticsearch_Logstash_Kibana/blob/master/ES2.3_with_Python(Push%20Data).md
