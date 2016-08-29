#### Install Elasticsearch 2.3.3 on ubuntu14.04
```
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer
wget  https://download.elastic.co/elasticsearch/release/org/elasticsearch/distribution/zip/elasticsearch/2.3.3/elasticsearch-2.3.3.zip
unzip  elasticsearch-2.3.3.zip
cd /elasticsearch-2.3.3
vim config/elasticsearch.yml
```
```
network.host: localhost
```
curl -X GET 'http://localhost:9200'

curl -X POST 'http://localhost:9200/tutorial/helloworld/1' -d '{ "message": "Hello World!" }'

curl -X GET 'http://localhost:9200/tutorial/helloworld/1'
```
#cluster.name: Admin_Cluster
#node.name: "Jerry DataCenter"
#http.port: 9200
#script.disable_dynamic: true
```
https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-elasticsearch-on-ubuntu-14-04

http://tecadmin.net/install-elasticsearch-on-linux/

http://javacore.cn/page/146/elasticsearch-233-ubuntu-under-the-installation-configuration-boot.html

https://github.com/rippleblue/Elasticsearch_Logstash_Kibana/blob/master/ES2.3_with_Python(Push%20Data).md
