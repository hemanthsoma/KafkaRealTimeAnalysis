## Meetup.com Real-Time Analytics 

The concept of real time analytics assumes ever increasing importance with more and more data coming from smart connected devices. The constant stream of data that is coming from these connected systems is unique in its volume, variety and velocity. Ingesting, analyzing and presenting these highly unstructured data assumes significance as it will throw insights in real time that will help businesses make decisions quicker.

In our project we wanted to dig deeper into this exciting field of real time analytics and get an insight into the technologies and the working of the real time streaming analytics. Hence, we analyzed the real time RSVP data of meetup.com to get real-time insights such as trending topics, cities etc. along with other business insights related to Meetups RSVPs. 

We utilized Apache Kafka for building real-time pipelines and Apache Spark to do real-time analysis and matplotlib for visualization. As and when an RSVP response is made by a user, our Kafka Producer receives that message through meetup’s web socket and feeds it to a topic. Then Kafka’s Consumer which has subscribed to that topic sends it to Spark’s streaming platform where only the U.S. messages are filtered and real time analysis to get the trending cities within the U.S. takes place. Then the results of the analysis get stored to a text file in our local system, using which visualizations is done in near real time using matplotlib. 

This project can be extended to get the real time trending topics across the world or for a specific geography along with other business insights. By giving real time trends in topics like in twitter, users of meetup will be aware of the more popular and less popular topics in near real time. With minor modifications, this project can also be extended to process and analyze IoT data.

## Technologies Used

* Kafka
* pySpark- version 2.4.7
* Python - version 3.0
* SparkSQL

## Features

List of features ready

* RSVP response is made by a user, our Kafka Producer receives that message through meetup’s web socket and feeds it to a topic.
* Then Kafka’s Consumer which has subscribed to that topic sends it to Spark’s streaming platform where only the U.S. messages are filtered and real time analysis to get the trending cities within the U.S. takes place. 
* Then the results of the analysis get stored to a text file in our local system, using which visualizations is done in near real time using matplotlib.

TODOs for future development

This project can be extended to get the real time trending topics across the world or for a specific geography along with other business insights. By giving real time trends in topics like in twitter, users of meetup will be aware of the more popular and less popular topics in near real time. With minor modifications, this project can also be extended to process and analyze IoT data.

## Getting Started and Usage

   Steps to consume the Meetup.com RSVP Stream
   1. Navigate to Kafka root directory 
          $ cd kafka_2.11-0.9.0.1 
   2. Start the Zookeeper by executing the below command 
          $ bin/zookeeper-server-start.sh config/zookeeper.properties 
   3. Start the Kafka Server 
          $ bin/kafka-server-start.sh config/server.properties
   4. Execute the Producer.py 
          $ ./Producer.py 
   5. Execute the Consumer.py file 
          $ ./Consumer.py

## Contributors

> Here list the people who have contributed to this project.
  * Sailash R
  * Hemanth Ghosh
  * Manaswini Agrawal
  * Swati Pralhad Chavhan
  * Pooja Kumari
  * Divya Peddireddy
  * Rajkumar K
  * Ashish Kumar
  * Aparna Sankarasetti
  * Devansh Sharma
  * Rohit Rawat 
  * Shubham Mishra
  * Vaibhav Kant mishra
  * Hemanth Soma
  * Mallakunta Suresh
  * Patrayadi Aditya Kumar
  * Yusuf Ansari
  * Jayashree C S

## Reference
* https://www.infoq.com/articles/apache-kafka 
* https://www.infoq.com/articles/apache-spark-streaming 
* https://www.vultr.com/docs/how-to-install-apache-kafka-on-centos-7 
* http://www.cloudera.com/documentation/enterprise/5-5-x/topics/spark_ipython.html 
* http://searchcrm.techtarget.com/definition/real-time-analytics 
* https://www.techopedia.com/2/31433/trends/big-data/advantages-of-real-time-analyticsfor-enterprise 
