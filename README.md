PersonalRestAPI is a Spring Boot REST API for learning purpose. Have the capabilities to run both on embedded tomcat and on external tomcat.

Dependencies: Maven will takecare of all the JAR/Library dependecies but you need to install MySQL DB for database. You can also change the configuration DB for other external or in memeory DB.

After installation of MySQL DB you need to have Person table on your DB.

Here is the create query: 
CREATE TABLE Person (PersonId varchar(255), FirstName varchar(255), MiddleName varchar(255), LastName varchar(255), Age int, Gender varchar(255));

Run this maven command to create a jar artifact <b> mvn clean package -Pjar </b>
Run this maven command to create a war artifact <b> mvn clean package -Pwar </b>

To run the jar file navigate to the targat folder in command prompt then run this command <b> java - jar PersonalInformationRestAPI-0.0.1-SNAPSHOT.jar </b>
Hit this URL <b> http://localhost:8080/welcomemessage </b>after the successful start of embbeded tomcat. You everything goes well you will get this message <b> Welcome to Personal Information Portal </b>

To run the war file, deploye it on the external tomcat.
Hit this URL <b> http://localhost:8080/<applicationcontext>/welcomemessage </b>after the successful start of embbeded tomcat. You everything goes well you will get this message <b> Welcome to Personal Information Portal </b>
Here applicationcontext is PersonalInformationRestAPI-0.0.1-SNAPSHOT

Steps to test the war file
1. To test PersonalInformationRestAPI-0.0.1-SNAPSHOT.war file deploy the war file on external Tomcat (I used Tomcat Version 11)
2. My ClientApplication will give you a war. Deploy the war on tomcat. Before doing the build read the readme file on ClientApplication repository.
3. Hit the URL, You will have a page tab to create record and other tab to view the record.
4. Any issue you can message me. 
