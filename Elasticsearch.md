#### Install Elasticsearch 2.3.3 on ubuntu14.04
```
sudo apt-get install software-properties-common
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get -y install oracle-java8-installer
curl -L -O https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-5.1.2.tar.gz
tar -xvf elasticsearch-5.1.2.tar.gz
cd elasticsearch-5.1.2
vim config/elasticsearch.yml
```
```
network.host: 127.0.0.1
cluster.name: Admin_Cluster
node.name: "Jerry DataCenter"
http.port: 9200
script.disable_dynamic: true
```
```
cd /home/lab/es/elasticsearch-2.3.3/bin
./elasticsearch
```
```
vi /etc/rc.local
su - lab -c "/home/lab/es/elasticsearch-2.3.3/bin/elasticsearch -d"
```
curl -X GET 'http://localhost:9200'

curl -X POST 'http://localhost:9200/tutorial/helloworld/1' -d '{ "message": "Hello World!" }'

curl -X GET 'http://localhost:9200/tutorial/helloworld/1'
```

```
https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-elasticsearch-on-ubuntu-14-04

http://tecadmin.net/install-elasticsearch-on-linux/

http://javacore.cn/page/146/elasticsearch-233-ubuntu-under-the-installation-configuration-boot.html

https://github.com/rippleblue/Elasticsearch_Logstash_Kibana/blob/master/ES2.3_with_Python(Push%20Data).md
