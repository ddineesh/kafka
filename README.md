Kafka Message Anatomy:

		key - binary  value - binary
			
			Compression Type
		(none, gzip, snappy, lz4, zstd) 	
		
			Headers ( Optional )
			
			Key1	Value1
			Key2 	Value2
		
			Partition + Offset
			
			Timestamp ( System 0r User set)
			

 Kafka Cluster - Collection of Brokers  ( which consists of topics, partitions, replications, partition leader & in-sync-replicas ( ISR ) and offsets topics
 
 Source System - > Producers -> 	Kafka Cluster     -> Consumers        ->		Target Systems
					round robin		Broker1				 Consumer offsets
					Key based order Broker2				 Consumer groups
					acks strategy   Broker3				 at least once 	
														 at most Once
									Zookeeper
									leader follower
									broker management
									
									


Usefule links:

https://www.conduktor.io/kafka/starting-kafka/

Starting the kafka 
https://www.conduktor.io/get-started/