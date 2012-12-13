Hello Java 67
=============

This simple servlet displays a brief hello message including the Java
version and Java vendor.

### Maven

Make sure you have [Maven](http://maven.apache.org/ "Maven") installed.
Then, *cd* into the root directory and execute:

	mvn clean package

That will create the *hellojava67.war* file within the 'target' directory.

### stackato.yml

Specify the desired Java runtime (java, java6, or java7) in the
stackato.yml file as follows:

     name: hellojava67

     framework:
       type: java_web
       runtime: java

     mem: 512M


Running the Application
-----------------------

To run the application:

  * mvn package

  * cp stackato.yml target

  * cd target

  * edit stackato.yml to change runtime to java/java6/java7 as desired

  * stackato push -n



The visit the app URL to see the Java version and vendor:

   Hello from 192.168.3.246:3000
    Java Version: 1.7.0_09 from Oracle Corporation
