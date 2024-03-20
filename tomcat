class-1
----------
TOMCAT:
PROCESS:
->create ec2-machine in amazon linux 2
->use t2.micro and pem key 
->tomcat port number is 8080
->go to root----->cd /opt
->amazon-linux-extras install java-openjdk11 -y
->https://tomcat.apache.org/download-90.cgi
->to download tomcat using zip ----->https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.87/bin/apache-tomcat-9.0.87.zip
->unzip https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.87/bin/apache-tomcat-9.0.87.zip
->rm -rf https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.87/bin/apache-tomcat-9.0.87.zip
->go to browse ---->public_ip:8080---->nothing to display 
->cd apache-tomcat-9.0.87
->cd bin
->chmod 777 catalina.sh
->chmod 777 startup.sh
->sh startup.sh
->go to browse ---->public_ip:8080---->it will display tomcat apachae application
->Goto "Manager App" in tomcat webpage 403 Access Denied
->how to reslove this?=====> goto the path
->go to webapps--->manager--->META-INF
->nano context.xml----->update the context.xml =====>
		allow=".*"
->Update the tomcat-users.xml file in /opt/apache-tomcat-9.0.87/conf
		<tomcat-users>
		<role rolename="manager-gui"/>
		<user username="admin" password="admin" roles="manager-gui, manager-script, manager-admin, manager-status"/>
		</tomcat-users>
->login to tomcat using
		user name:admin
		password:Admin
->installation completed

DEPLOYMENT:
->cd /opt/apache-tomcat-9.0.87/webapps/
->deploy a sample .war file [What ever the .war files present in webapps folder tomcat will deploy those]
->try below sample war files and try to access from tomcat
->wget https://tomcat.apache.org/tomcat-7.0-doc/appdev/sample/sample.war
->wget https://updates.jenkins.io/download/war/2.416/jenkins.war

ADVANCED STEPS:
->to change the tomcat default port number from 8080 to other port [ex: 8081]
->goto /opt/tomcat9/conf
->cd /opt/tomcat9/conf
->cat server.xml | grep 8080
->change connector port from 8080 to 8081
->restart tomcat [/opt/tomcat9/bin--------> shutdonw.sh then startup.sh]

Tomcat_Jenkins integration:
Plug-in used to integrate Tomcat with Jenkins=============>"Deploy to container" [incase of freestyle project]
Plug-in used to integrate Tomcat with Jenkins=============>"ssh agent" [incase of pipline project]








OUTSIDE MATERIAL:
---------------------
Tomcat installation steps
Launch instance with java pre-intalled

To donwload tomcat to our ubuntu machine/inatance

cd /opt

sudo wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.80/bin/apache-tomcat-9.0.80.tar.gz
wget======> to download files from web

In order to avoid permisson denied errors
sudo su---- to become root/super user
sudo su
Unzip/ tar the file use below command
tar -xvzf apache-tomcat-9.0.80.tar.gz
Rename folder to tomcat9
mv apache-tomcat-9.0.80 tomcat9
goto the below path
cd /opt/tomcat9/bin
we need to start the tomcat server. so we need to execute the script in bin path
sh startup.sh
Tomcat has started in step-7, now we can able access the tomcat from web
publicip:8080

Goto "Manager App" in tomcat webpage 403 Access Denied

how to reslove this?=====> goto the path

cd /opt/tomcat9/webapps/manager/META-INF
update the context.xml =====>allow=".*"

Update the tomcat-users.xml file in /opt/tomcat9/conf
<tomcat-users>
<role rolename="manager-gui"/>
<user username="admin" password="Admin" roles="manager-gui, manager-script, manager-admin, manager-status"/>
</tomcat-users>
login using below creds
user name:admin
password:Admin

cd /opt/tomcat9/webapps

deploy a sample .war file [What ever the .war files present in webapps folder tomcat will deploy those]

try below sample war files and try to access from tomcat

wget https://tomcat.apache.org/tomcat-7.0-doc/appdev/sample/sample.war

wget https://updates.jenkins.io/download/war/2.416/jenkins.war



Advanced steps
to change the tomcat default port number from 8080 to other port [ex: 8081]
goto /opt/tomcat9/conf
cd /opt/tomcat9/conf
cat server.xml | grep 8080
change connector port from 8080 to 8081
restart tomcat [/opt/tomcat9/bin--------> shutdonw.sh then startup.sh]

Tomcat_Jenkins integration
Plug-in used to integrate Tomcat with Jenkins=============>"Deploy to container" [incase of freestyle project]
Plug-in used to integrate Tomcat with Jenkins=============>"ssh agent" [incase of pipline project]
