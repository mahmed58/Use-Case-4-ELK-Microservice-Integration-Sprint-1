Elasticsearch--[version 2.3.4] [t2.micro EC2 instance supports only 2.3.X version]

Prerequisites
•	Configuration of AWS EC2 Instance Amazon Linux/Ubuntu Machine with t2.micro for ElasticSearch [I am using Ubuntu AMI for this demo]
•	Java Installation [Command : sudo apt-get update && sudo apt install openjdk-8-jdk]


Installation of ElasticSearch AWS EC2 Instance:

Step 1: Download the Elastic Search DEB file.

wget https://download.elastic.co/elasticsearch/release/org/elasticsearch/distribution/deb/elasticsearch/2.3.4/elasticsearch-2.3.4.deb
 
Step 2: unpack Elastic Search

dpkg -i elasticsearch-2.3.4.deb

Step 3: Change Elastic Search Configuration file. Sample file is uploaded in the ElasticSearch folder

cd /etc/elasticsearch
vi elasticsearch.yml
cluster.name: tfs_india
index.number_of_shards: 5
index.number_of_replicas: 0

node.name: tfs_india_node_1

network.host: <network_hostname>
 
And save above configuration.

Step 4: Start Elastic Search Service and check the status

sudo /etc/init.d/elasticsearch status

sudo /etc/init.d/elasticsearch start
 
curl -XGET http://localhost:9200/ to check the elasticserach is running.
 
Step 5: To stop elasticsearch service.

service elasticsearch stop
