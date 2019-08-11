# Topics, Brokers ##

## Topic ##
- Particular steam of data, similar to a table in DB
- Topic is identified by its name
- Topics are spilt in partitions and each message within a partition has an Offset
- By default, data is kept only for a limited time (default is 1 week)
- Once data is written, it cannot be changed

## Brokers ##
- Kafka cluster consists of multiple servers (brokers)
- Broker is identified with its id which **SHOULD BE AN INTEGER**
- Each broker contains only certain partitions
- Once connected to any broker (called bootstrap broker) you get connected to the entire cluster

## Topic Replication Factor ##
- Topics should have replication factor of > 1 - usually 2 or 3 (considered as gold standard)
