                          
 *******************************************
 *                                         *
 *  First Hello                            *
 *  World program                          *
 *                                         *
 *  Using the Spring MVC framework         *
 *                                         *             
 *******************************************


Intent of this App:
To learn what a controller is and how it connects to the "view" of MVC.



This has NOT been setup, tested or run on a Windows
platform. If one wants to try on a Windows platform, please make sure all variables are set correctly.
This hello world project was build using the following:

Hardware:
  - MacBook Pro 15 in
       * OS X Maverick 10.9.3
       * 4 GB DDR3
	   * 2.66 GHz Intel Core 2 Duo

Software:
  - Eclipse IDE for Java EE Developers (https://www.eclipse.org/downloads/index-developer.php?release=kepler)
        * Kepler 4.3.2 (x64 bit)
  - Spring Tool Suite 3.5.1 (http://spring.io/guides/gs/sts/)
  - Tomcat 7.0.52 (http://tomcat.apache.org/download-70.cgi#7.0.53)
        * used Core > tar.gz file
  - Git 1.9.2
  - Chrome
  

Instructions:

Note: Please make sure that java and maven have been properly installed. If not, the maven and java commands 
      in Step 4 below will not work. 
      Need Help installing? See Links section below for more information details.

Setup:
 Through the Eclipse Marketplace, make sure the following have been added:
   - Spring Tool Suite (STS)

 Check the java version you have on the command prompt by running the following command:
    java -v

 Check to see if maven has been installed by running the following command at the command prompt 
 (inside the root directory, helloWorld): 
     mvn --version

To run (once the above has been checked and verified):

  1) Checkout or unzip the project to a designated project folder
  2) Start Eclipse
  3) open a command prompt, navigate to the springProjects/helloWorld folder
  4) Run the following commamnd:
        mvn clean package && java -jar target/gs-serving-web-content-0.1.0.jar
  5) Open up a browser and head to 'http://localhost:8080/greeting'.
  6) Hello World!! should appear. 

Alternate run:

For steps 5 & 6, you can append '?name=<your name here>' which will output 'Hello, <whatever you put>!!' instead
of the traditional Hello, World!!.


Lessons Learned:
controller - Handles the request and returns the appropriate model and view.
             In this case, there was one model. The GreetingController has a method called greeting
			 that maps to the views resource/spring directory greeting.html view (V of the 'MVC'). The GreetingController
			 returns greeting.

model -      Binds the name to the name paramter that is being passed in on the greeting method.
             The name value is not used by default. However you can use it if you would like. Just have to 
		     append it to the end of the localhost URL. See 'Alternate run' above.

view -       What the user sees. Here I am using Thymeleaf which performs the server side html renderings.
             th:text is evaluated.


Links:

 Java:              http://www.java.com/en/download/mac_download.jsp?locale-=en
 Maven:             http://maven.apache.org/
 Tomcat:            http://tomcat.apache.org/download-70.cgi
 Spring Tool Suite: http://marketplace.eclipse.org/content/spring-tool-suite-sts-eclipse-kepler-43#.U3k_71hdVE8
 Git:               http://git-scm.com/downloads

