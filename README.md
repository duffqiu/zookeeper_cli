# zookeeper-cli
the zookeeper client tool in docker container

### using below command to test zookeeper
- docker run -it duffqiu/zookeeper_cli -server <zookeeper ip>:2181

- note: if you run the zookeeper server under the same docker, it seems we can't user 127.0.0.1 for the <zookeeper ip>. we need to use the docker0 ip.


### dynamic fetch the docker0 ip when run the container.

- `# docker0_ip=$(/usr/bin/ip -o -4 addr list docker0 | grep global | awk '{print $4}'| cut -d/ -f1)`
- `# docker run -it --rm duffqiu/zookeeper-cli -server $docker0_ip:2181`
- note: you also can use the eth0's ip
