Kibana--[Version-4.5.2]

Prerequisites
•	Configuration of AWS EC2 Instance Amazon Linux/Ubuntu Machine t2.micro. [I am using Ubuntu AMI for this demo]
•	Java Installation [Command : sudo apt-get update && sudo apt install openjdk-8-jdk]

Installation on AWS Kibana EC2 Instance

Step 1: Download the Kibana RPM file.

wget https://download.elastic.co/kibana/kibana/kibana_4.5.2_amd64.deb
 
Step 2: unpack Kibana

dpkg -i kibana_4.5.2_amd64.deb

Step 3: Change Kibana Configuration file to point it to ElasticSearch EC2 AWS instance public ip. Sample file for the same is uploaded in kibana folder in git. 
cd /etc/kibana
vi kibana.yml
 
 
Step 4: Start Kibana Service
service  kibana start
service kibana status
 

 
Step 5: To stop kibana service.
service kibana stop
