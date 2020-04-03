Logstash--[version 2.3.4] [t2.micro supports only 2.3.X version]


Prerequisites
•	Configuration of AWS EC2 Instance Amazon Linux/Ubuntu Machine t2.[I am using Ubuntu AMI for this demo]
•	Java Installation [Command : sudo apt-get update && sudo apt install openjdk-8-jdk]

Installation of Logstash AWS EC2 Instance

Step 1: Download the Logstash DEB file.
wget https://download.elastic.co/logstash/logstash/packages/debian/logstash_2.3.4-1_all.deb

Step 2:  unpack Logstash
dpkg -i logstash_2.3.4-1_all.deb

Step 3: Create Logstash Configuration file under /opt/logstash/bin. Sample file is uploaded in the Logstash folder
cd /opt/logstash/bin 
 
vi logstash-sample.conf

see logstash-sample.conf 
 
Step 4: Start logstash Service

sudo /etc/init.d/logstash start

sudo /etc/init.d/logstash status
 
Step 5: To stop logstash service.
sudo /etc/init.d/logstash start
