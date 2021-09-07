# docker&zk

登录zk

![image-20210901141316899](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210901141316899.png)

查看目录

![image-20210901141400023](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210901141400023.png)

zkCli.sh [-server ip:port]   例：zkCli.sh -server 127.0.0.1:2181

ls /      //查看zk节点

ls2 /    //查看zk节点 附带统计信息

create [-s][-e] path data acl //创建节点  [-s]顺序追加，持久节点  [-e]临时节点，quit退出zk session就删除

           create -s  /zk-test "123"
    
           create -s  /zk-test "456"
    
           create -s  /zk-test "789"


           create -e /zk-test123 临时节点，随zk session退出自动删除

delete  //删除节点

           delete /zk-test

get     //获取节点信息，创建节点 zk-123 赋值test-abc,此时运行 get /zk-123 就能获取到节点信息 test-abc

​

set   //更新节点信息

connect host:port    连接到指定节点

setquota -n|-b val path 某个Znode指定多少存储空间或者允许创建多少个节点

n 指定可以设置多少个子节点

b 指定可以设置多大空间（byte）



listquota path

对于配额不是硬性的提示，超过配额还是可以继续创建，只不过在日志里面有提示

stat path查看节点的状态



---

# kafka

```bash
/opt/kafka/bin/kafka-console-consumer.sh --zookeeper localhost:2181 --topic show --from-beginning
```

WARN [Consumer clientId=consumer-console-consumer-93884-1, groupId=console-consumer-93884] Bootstrap broker localhost:9092 (id: -1 rack: null) disconnected (org.apache.kafka.clients.NetworkClient



/opt/kafka/bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic mbs_mq_dto_kafka

