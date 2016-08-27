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
