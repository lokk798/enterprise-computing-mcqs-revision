# Apache Kafka Multiple Choice Questions

## 1. What is the primary purpose of an Enterprise Service Bus (ESB)?

- A) To serve as a database management system
- B) To provide a centralized communication backbone for application integration
- C) To replace message queues entirely
- D) To act as a substitute for API management

**Correct Answer: B**

---

## 2. In the context of Kafka, what does the term "broker" refer to?

- A) A client that produces messages
- B) A server process that manages a set of topics
- C) A consumer that reads messages
- D) The API gateway that routes requests

**Correct Answer: B**

---

## 3. What was the main reason LinkedIn developed Kafka?

- A) To replace their traditional database systems entirely
- B) To handle high message throughput that existing systems couldn't manage
- C) To create a new open-source project for Apache
- D) To create a more complex messaging system

**Correct Answer: B**

---

## 4. What is the relationship between Kafka Topics and Partitions?

- A) Topics are subsets of partitions
- B) A topic has one or more partitions which are physical logs
- C) Partitions can exist without topics
- D) Topics and partitions are synonymous terms

**Correct Answer: B**

---

## 5. What is the role of Apache Zookeeper in a Kafka system?

- A) It replaces Kafka brokers in newer versions
- B) It manages metadata and decides which broker is responsible for which topic
- C) It handles message serialization and deserialization
- D) It stores all messages that pass through Kafka

**Correct Answer: B**

---

## 6. What happens to the total message ordering when a topic has multiple partitions?

- A) Total ordering is maintained across all partitions
- B) Only partial orders exist per partition, and total ordering is lost
- C) Messages are automatically reordered by consumers
- D) Zookeeper maintains total ordering across partitions

**Correct Answer: B**

---

## 7. In Kafka, what does "isr" stand for and what does it represent?

- A) Internal System Registry - the internal database of brokers
- B) In-Sync Replicas - brokers that have successfully replicated messages
- C) Intermediate Storage Repository - where messages are temporarily stored
- D) Interconnected Service Responders - consumers connected to brokers

**Correct Answer: B**

---

## 8. What happens when the value of "isr" becomes less than the replication factor?

- A) The cluster immediately stops operating
- B) The cluster continues to operate but does not compensate for the missing replicas
- C) Zookeeper automatically creates new replicas
- D) Messages are redirected to other topics

**Correct Answer: B**

---

## 9. What is the default message retention period in Kafka?

- A) 24 hours
- B) 72 hours
- C) 168 hours (7 days)
- D) Forever, unless manually deleted

**Correct Answer: C**

---

## 10. Which of the following correctly describes a Kafka offset?

- A) The physical distance between brokers in a cluster
- B) A bookmark that corresponds to the position of the last consumed message
- C) The number of partitions assigned to a topic
- D) The time delay between message production and consumption

**Correct Answer: B**

---

## 11. What is the significance of using KafkaTemplate in Spring Kafka?

- A) It's only used for testing Kafka applications
- B) It's a wrapper that simplifies sending messages to Kafka topics
- C) It replaces the need for brokers in a Kafka system
- D) It converts JSON messages to String format

**Correct Answer: B**

---

## 12. In Kafka Producer configuration, what does setting "acks=2" mean?

- A) At least two consumers must acknowledge receiving the message
- B) The message must be acknowledged by the leader and all in-sync replicas
- C) Two copies of each message will be created
- D) The producer will retry sending a failed message twice

**Correct Answer: B**

---

## 13. What's the purpose of a Consumer Group in Kafka?

- A) To ensure all consumers receive all messages
- B) To distribute message consumption load across multiple consumers
- C) To prevent any message consumption
- D) To create a hierarchy of consumers

**Correct Answer: B**

---

## 14. What happens when there are more consumers in a Consumer Group than partitions in a topic?

- A) The extra consumers will be idle
- B) The partitions will be split between all consumers
- C) New partitions will be automatically created
- D) The system will raise an error

**Correct Answer: A**

---

## 15. What does "auto-commit = true" mean in a Kafka consumer configuration?

- A) Messages are automatically deleted after being read
- B) The consumer automatically sends its latest offset to the broker periodically
- C) Producers automatically resend failed messages
- D) The consumer will automatically join a consumer group

**Correct Answer: B**

---

## 16. Which special topic does Kafka use to manage consumer offsets?

- A) \_\_kafka_offsets
- B) \_\_consumer_positions
- C) \_\_consumer_offsets
- D) \_\_offset_manager

**Correct Answer: C**

---

## 17. What happens during a "rebalancing" operation in Kafka?

- A) Messages are redistributed among all topics
- B) Partitions are reassigned among consumers in a group
- C) Brokers are redistributed across the physical servers
- D) The workload is balanced between producers and consumers

**Correct Answer: B**

---

## 18. When implementing a message handler with @KafkaListener in Spring, what does adding "isDefault = true" to a @KafkaHandler method accomplish?

- A) It makes the method handle all message types not specifically handled by other methods
- B) It makes the method execute before any other handlers
- C) It prevents the method from handling any messages
- D) It forces all messages to be processed by this method only

**Correct Answer: A**

---

## 19. In Kafka, what is the relationship between one consumer (in a group) and partitions?

- A) One consumer can only consume from one partition
- B) One partition can be assigned to multiple consumers in the same group
- C) One partition is assigned to one consumer in a group
- D) Consumers don't directly interact with partitions

**Correct Answer: C**

---

## 20. What is the primary advantage of setting "enable.auto.commit = false" in a Kafka consumer?

- A) It improves message processing speed
- B) It prevents message loss in case of consumer failures
- C) It allows consuming messages from multiple topics
- D) It reduces network traffic between the consumer and broker

**Correct Answer: B**
