
### Kafka

Apache Kafka is a distributed publish-subscribe messaging system and a robust queue that can handle a high volume of data and enables you to pass messages from one end-point to another. Kafka is suitable for both offline and online message consumption. Kafka messages are persisted on the disk and replicated within the cluster to prevent data loss. Kafka is built on top of the ZooKeeper synchronization service. It integrates very well with Apache Storm and Spark for real-time streaming data analysis.
Benefits

Following are a few benefits of Kafka −

    Reliability − Kafka is distributed, partitioned, replicated and fault tolerance.

    Scalability − Kafka messaging system scales easily without down time..

    Durability − Kafka uses "Distributed commit log" which means messages persists on disk as fast as possible, hence it is durable..

    Performance − Kafka has high throughput for both publishing and subscribing messages. It maintains stable performance even many TB of messages are stored.

### Components and Description

* **Topics:** <br/>

  A stream of messages belonging to a particular category is called a topic. Data is stored in topics.

  Topics are split into partitions. For each topic, Kafka keeps a mini-mum of one partition. Each such partition contains messages in an immutable ordered sequence. A partition is implemented as a set of segment files of equal sizes.
 	

* **Partition:** <br/>

  Topics may have many partitions, so it can handle an arbitrary amount of data.
 	

* **Partition offset:**<br/>

  Each partitioned message has a unique sequence id called as "offset".
	

* **Replicas of partition:**<br/>

  Replicas are nothing but "backups" of a partition. Replicas are never read or write data. They are used to prevent data loss.
	

* **Brokers:**<br/>

  Brokers are simple system responsible for maintaining the pub-lished data. Each broker may have zero or more partitions per topic.

* **Kafka Cluster:**<br/>

  Kafka’s having more than one broker are called as Kafka cluster. A Kafka cluster can be expanded without downtime. These clusters are used to manage the persistence and replication of message data.


* **Producers:**<br/>

  Producers are the publisher of messages to one or more Kafka topics. Producers send data to Kafka brokers. Every time a producer pub-lishes a message to a broker, the broker simply appends the message to the last segment file. Actually, the message will be appended to a partition. Producer can also send messages to a partition of their choice.


* **Consumers:**<br/>

  Consumers read data from brokers. Consumers subscribes to one or more topics and consume published messages by pulling data from the brokers.


* **Leader:**<br/>

  "Leader" is the node responsible for all reads and writes for the given partition. Every partition has one server acting as a leader.

* **Follower:**<br/>

  Node which follows leader instructions are called as follower. If the leader fails, one of the follower will automatically become the new leader. A follower acts as normal consumer, pulls messages and up-dates its own data store.

