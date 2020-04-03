README.md


Deploying your microservices in AWS EC2 instance --

1. Run your microservice spring boot application in your local system configuring the logback xml 
2. Package it as a JAR
3. Copy the same Jar file from your local system to AWS EC2 instance of your microservice using WINSCP application
4. Start filebeat
5. Run your micriservice application using java -jar <NAME>
6. Logs with be generated in the logback file specified in your application 
7. Same logs will be picked up by filebeat and send to Logstash then to elastic search