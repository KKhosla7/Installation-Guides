# Install Apache Kafka on Mac using Homebrew

This procedure explains how to install **Zookeeper** and **Kafka** using **Homebrew** on **MacOS**

## Install Kafka

* Install **Kafka**: `$ brew install kafka`
* Install **Homebrew services**: `$ brew tap homebrew/services`
* Start and now restart at login. __Please see **Notes #1** before you execute below sub commands.__
  * **Zookeeper**: `$ brew services start zookeeper` 
  * **Kafka**: `$ brew services start kafka`
* Verify **Zookeeper and Kafka services** is up and running: `$ brew services list`

## Create a Kafka Topic

> A topic is a category or feed name to which records are published. Topics in Kafka are always multi-subscriber; that is, a topic can have zero, one, or many consumers that subscribe to the data written to it.

```$ kafka-topics --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic test```

Here we have created a topic name `test`

## Initialize Producer Console

Now we will initialize the Kafka producer console, which will listen to localhost at port `9092` at topic test :

`$ kafka-console-producer --broker-list localhost:9092 --topic test`

```
>First Message
>Second Message
>Third Message
```

## Initialize Consumer Console

Now we will initialize the Kafka consumer console, which will listen to bootstrap server localhost at port `9092` at topic test from beginning:

`$ kafka-console-consumer --bootstrap-server localhost:9092 --topic test --from-beginning`

```
First Message
Second Message
Third Message
```
## List Of Topics Created

You can also get the list of topics created

`$ kafka-topics --list --zookeeper localhost:2181`

## Notes

1. If you don't want/need a background service you can just run: ```$ zookeeper-server-start /usr/local/etc/kafka/zookeeper.properties & kafka-server-start /usr/local/etc/kafka/server.properties```. It will install Zookeeper and Kafka.
