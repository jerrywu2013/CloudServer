###Install ClickHouse on Ubuntu14.04

```
nano /etc/apt/sources.list
deb http://repo.yandex.ru/clickhouse/trusty/ stable main

```
```
apt-key adv --keyserver keyserver.ubuntu.com --recv E0C56BD4
wget -q -O - https://repo.yandex.ru/clickhouse/CLICKHOUSE-KEY.GPG | apt-key add -
apt-get update
apt-get install clickhouse-server-common clickhouse-client -y
service clickhouse-server start
```
###Getting Started 
```
clickhouse-client 
```
