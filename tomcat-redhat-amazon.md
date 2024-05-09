# To install Tomcat on redhat or amazon linux

## Install Java
`sudo yum install java-1.8*`

## Install Tomcat
* `sudo su -`
* `cd /opt`

## Download tomcat binary
`wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz`

## unzip tomcat binary
`tar -zvxf apache-tomcat-9.0.89.tar.gz`

## Add Execute Permission to startup.sh & shutdown.sh
* `cd apache-tomcat-9.0.89/bin`
* `chmod +x startup.sh`
* `chmod +x shutdown.sh`

## Create link files for Tomcat Server up and Down
* `ln -s /opt/apache-tomcat-9.0.89/bin/startup.sh /usr/local/bin/tomcatup`
* `ln -s /opt/apache-tomcat-9.0.89/bin/shutdown.sh /usr/local/bin/tomcatdown`
* `tomcatup`
* `tomcatdown`

## Change Settings to Manage Tomcat
### To Access Manager App
1. Delete or Comment `<Valve>`tag in context.xml file.
   **Location** : `/opt/apache-tomcat-9.0.89/webapps/manager/META-INF/context.xml`
2. Add Users and Roles in tomcat-users.xml file.
   **Location** : `/opt/apache-tomcat-9.0.89/conf/tomcat-users.xml`

* [context.xml](https://github.com/Harshavardhan-Sure/Tomcat/blob/main/context.xml)
* [tomcat-users.xml](https://github.com/Harshavardhan-Sure/Tomcat/blob/main/tomcat-users.xml)


`http://server_ip:8080/`

 Now we can Access Tomcat welcome page.
