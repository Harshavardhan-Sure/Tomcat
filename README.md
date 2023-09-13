# Tomcat 

## To install tomcat on ubuntu 

* `sudo apt-get update`
* `sudo apt-get install jdk-11-jdk -y`
* `cd /opt`  or   `cd /tmp`
* `wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.80/bin/apache-tomcat-9.0.80.tar.gz`
* `sudo tar -xvzf /opt/apache-tomcat-9.0.*tar.gz -C /opt/tomcat9 --strip-components=1`

## Start Tomcat Server
### Go to   `cd /opt/tomcat9/bin`
* To Start  :  `./startup.sh` 
* To Stop   :  `./shutdown.sh`

### To Access Manager App:
1. Delete or Comment `<Valve>`tag in context.xml file.
   **Location** : `/opt/tomcat9/webapps/manager/META-INF/context.xml`
2. Add Users and Roles in tomcat-users.xml file.
   **Location** : `/opt/tomcat9/conf/tomcat-users.xml`

After Editing these xml files `Restart Tomcat`
* `./shutdown.sh`
* `./startup.sh`
 

