# To install Tomcat on redhat or amazon linux

## Install Java
`sudo yum install java-1.8*`

## Install Tomcat
* `sudo su -`
* `cd /opt`

## Download tomcat binary
`wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.55/bin/apache-tomcat-9.0.55.tar.gz`

## unzip tomcat binary
`tar -zvxf apache-tomcat-9.0.55.tar.gz`

## Add Execute Permission to startup.sh & shutdown.sh
* `cd apache-tomcat-9.0.55/bin`
* `chmod +x startup.sh`
* `chmod +x shutdown.sh`

## Create link files for Tomcat Server up and Down
* `ln -s /opt/apache-tomcat-9.0.55/bin/startup.sh /usr/local/bin/tomcatup`
* `ln -s /opt/apache-tomcat-9.0.55/bin/shutdown.sh /usr/local/bin/tomcatdown`
* `tomcatup`
* `tomcatdown`

## Change Settings to Manage Tomcat
* [context.xml](https://github.com/Harshavardhan-Sure/Tomcat/blob/main/context.xml)
* [tomcat-users.xml](https://github.com/Harshavardhan-Sure/Tomcat/blob/main/tomcat-users.xml)


`http://server_ip:8080/`

 Now we can Access Tomcat welcome page.
