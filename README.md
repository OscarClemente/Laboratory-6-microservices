# Web Engineering 2015-2016 / Microservices

##The two microservices are running and registered
![Account](https://raw.github.com/OscarClemente/Laboratory-6-microservices/master/screenshots/account1.png)
![WebService](https://raw.github.com/OscarClemente/Laboratory-6-microservices/master/screenshots/web1.png)

##The service registration service has the two microservices registered
![Both instances registered](https://raw.github.com/OscarClemente/Laboratory-6-microservices/master/screenshots/servicesregistered1.png)

##A second account microservice is running in the port 4444 and it is registered
![Account in the port 4444](https://raw.github.com/OscarClemente/Laboratory-6-microservices/master/screenshots/account2.png)

##A brief report describing what happens when you kill the microservice with port 2222. Can the web service provide information about the accounts? Why?
Yes, it will keep providing information about the accounts because although the 2222 fails it asks again for a service and as 4444 is alive it keeps working.