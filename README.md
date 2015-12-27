# Web Engineering 2015-2016 / Microservices

##The two microservices are running and registered
![Account](https://raw.github.com/OscarClemente/Laboratory-6-microservices/master/screenshots/account1.png)
![WebService](https://raw.github.com/OscarClemente/Laboratory-6-microservices/master/screenshots/web1.png)

##The service registration service has the two microservices registered
![Both instances registered](https://raw.github.com/OscarClemente/Laboratory-6-microservices/master/screenshots/servicesregistered1.png)

##A second account microservice is running in the port 4444 and it is registered
![Account in the port 4444](https://raw.github.com/OscarClemente/Laboratory-6-microservices/master/screenshots/account2.png)

##A brief report describing what happens when you kill the microservice with port 2222. Can the web service provide information about the accounts? Why?
When you kill the microservice with port 2222, the Web service Microservice, when you try to do an operation, first shows "Refused connection" errores. A few seconds after this, it shows "No instances available for ACCOUNTS-SERVICE". Finally, twenty or thirty seconds after this, it starts working again.

What actually happens is that, when the Account Microservice in port 2222 is shutted down, the WebService Microservice tries to communicate with it and fails. The Webservice Microservice got the Account Microservice address and port from the Service Registration, but now it is down. It takes the WebService Microservice a little time to realize that it is actually down, and then it asks the Service Registration for another Microservice that provides the ACCOUNTS-SERVICE service. The Service Registration asks it with the port of the another Microservice (4444), and then it starts working again.
