# Tomcat 

## To install tomcat on ubuntu 

* `sudo apt-get update`
* `sudo apt-get install openjdk-11-jdk -y`
* `cd /opt`  or   `cd /tmp`
* `wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.80/bin/apache-tomcat-9.0.80.tar.gz`
* `sudo tar -xvzf /opt/apache-tomcat-9.0.*tar.gz -C /opt/tomcat9 --strip-components=1`

## To Start Tomcat Server
### Go to   `cd /opt/tomcat9/bin`
* To Start  :  `./startup.sh` 
* To Stop   :  `./shutdown.sh`
* Access Tomcat Application from Browser on port 8080 `http://<Public_IP>:8080`

### To Access Manager App
1. Delete or Comment `<Valve>`tag in context.xml file.
   **Location** : `/opt/tomcat9/webapps/manager/META-INF/context.xml`
2. Add Users and Roles in tomcat-users.xml file.
   **Location** : `/opt/tomcat9/conf/tomcat-users.xml`

After Editing these xml files `Restart Tomcat`
* `./shutdown.sh`
* `./startup.sh`

### To Deploy WAR file to Tomcat Deployment Directory
* Paste WAR file in `/opt/tomcat9/webapps/`
* Sample WAR file : [Sample-WAR](https://github.com/Harshavardhan-Sure/Sample-WAR)
* To Access : `http://<Public_IP>:8080/myapp`


## Other Useful Commands
* To check out services are started or not :  `ps -ef | grep tomcat`

* To check permissions on startup.sh :  `ls -ltr`

* To Give Execution permissions `sudo chmod +x startup.sh` and `sudo chmod +x shutdown.sh`

### To Create Link files for startup.sh and shutdown.sh

* `ln -s /opt/tomcat9/bin/startup.sh /usr/local/bin/tomcatup`
* `ln -s /opt/tomcat9/bin/shutdown.sh /usr/local/bin/tomcatdown`

* To start and stop tomcat Use `tomcatup` `tomcatdown`

## Changing Tomcat Port Number
* Change port 8080 to desired port which are under HTTP ports
* `vim /opt/tomcat9/conf/server.xml`
    
 

