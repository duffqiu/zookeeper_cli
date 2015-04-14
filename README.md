# zookeeper_cli
the zookeeper client tool in docker container

### using below command to test zookeeper
- docker run -it duffqiu/zookeeper_cli -server <zookeeper ip>:2181

- note: if you run the zookeeper server under the same docker, it seems we can't user 127.0.0.1 for the <zookeeper ip>. we need to use the docker0 ip.
