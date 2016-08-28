#### Install Elasticsearch on ubuntu14.04
```
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer
wget https://download.elastic.co/elasticsearch/elasticsearch/elasticsearch-2.3.1.tar.gz
tar xzf elasticsearch-2.3.1.tar.gz
vim config/elasticsearch.yml
```
```
cluster.name: Admin_Cluster
node.name: "Jerry DataCenter"
network.host: localhost
http.port: 9200
script.disable_dynamic: true
```
curl -X GET 'http://localhost:9200'

https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-elasticsearch-on-ubuntu-14-04
http://tecadmin.net/install-elasticsearch-on-linux/
