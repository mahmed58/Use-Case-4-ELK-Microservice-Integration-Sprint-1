Filebeat--


Prerequisites
•	Configuration of AWS EC2 Instance Amazon Linux/Ubuntu Machine T2.Micro. [NOTE: This is the same EC2 instance which we have deployed microservice on]
•	Java Installation [Command : sudo apt-get update && sudo apt install openjdk-8-jdk]

Installation of FileBeat on AWS EC2 Instance same as Microservice EC2 instance
 
Step 1: Download the File beat DEB file.

wget https://download.elastic.co/beats/filebeat/filebeat_1.3.0_amd64.deb

Step 2: Install File Beat

dpkg -i filebeat_1.3.0_amd64.deb

Step 3: Change Filebeat Configuration file. Sample filebeat.yml is uploaded in Git. 
cd /etc/filebeat
vi filebeat.yml
 
Filebeat Input : Microservice Log Paths
 
Filebeat will maintain its own registry file to register the logs coming from Microservice. One registry file path need to mention in configuration.
 
Filebeat Output : Logstash machine details
 
Step 4: Start Filebeat Service
service  filebeat start
service filebeat status
 
Step 5: To stop filebeat service.
service filebeat stop
