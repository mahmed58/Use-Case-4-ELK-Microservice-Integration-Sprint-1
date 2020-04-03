# Use-Case-4-ELK-Microservice-Integration-Sprint-1


Project name:
	Installation & Integration of ELK Stack, Filebeat on AWS EC2 Instances with Microservices.


Description: 
	
	The ELK Stack consists of three open-source products - Elasticsearch, Logstash, and Kibana from Elastic. 
These three are used together for log analysis in various environments. 
So Logstash collects and parses logs, Elastic search indexes and store this information while Kibana provides a UI layer that provide actionable insights. 
FileBeats are lightweight data shippers that we install as agents on servers to send specific types of operational data to Logstash.
Microservices here used to collect logs to establish the above functionality and deployment environment AWS E2 Cloud Instances. 
This document will not cover how to configure AWS EC2 instances since it is out of scope for this article.

Overview of ELK Stack and FileBeat
E = Elasticsearch 
Elasticsearch is an open-source, RESTful, distributed search and analytics engine built on Apache Lucene. Support for various languages, high performance, and schema-free JSON documents makes Elasticsearch an ideal choice for various log analytics and search use cases.
L = Logstash
Logstash is an open-source data ingestion tool that allows you to collect data from a variety of sources, transform it, and send it to your desired destination. With pre-built filters and support for over 200 plugins, Logstash allows users to easily ingest data regardless of the data source or type. 
K = Kibana
Kibana is an open-source data visualization and exploration tool for reviewing logs and events. Kibana offers easy-to-use, interactive charts, pre-built aggregations and filters, and geospatial support and making it the preferred choice for visualizing data stored in Elasticsearch
File Beat
Filebeat is a lightweight shipper for forwarding and centralizing log data. Installed as an agent on your microservice servers, Filebeat monitors the log files or locations that you specify, collects log events, and forwards them either to Elasticsearch or Logstash for indexing.

