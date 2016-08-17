
####Installing Solr 5.5 on Ubuntu 14.04
```
sudo apt-get update && apt-get upgrade -y
sudo apt-get install python-software-properties
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer
cd /tmp
wget http://www.us.apache.org/dist/lucene/solr/5.5.2/solr-5.5.2.tgz
tar xzf solr-5.5.2.tgz
cd solr-5.5.2/bin/
sudo solr-5.5.2/bin/install_solr_service.sh solr-5.5.2.tgz
```
http://IP:8983/solr
