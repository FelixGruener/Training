# Code Challenge 

The Requirements didnt specify not to use Frameworks. I used the Spring Framework.

The Design and Architecture i chose intents to deliver a sustainable generic load csv import to DB  service. So the application can be used for any load of any csv to any MySQL DB Table. 

The Code can be tested by a Webpage calling 127.0.0.1/load . Once this Page is requested from embedded Tomcat Webserver the cvs gest loaded and inported to DB.

A REST Controller is called dispatching the request to a batch job. So the application can be used for any load of any csv to any MySQL DB Table. 

The CSV, DB ,Table and Connectivity can be configured in application.properties. This makes it highly reusable.

Though some assumptions remained:

Some Fields from csv were not included in the DB Scheme ? such as Sub-Category ?  I assumed this means not to support them ? The csv included Field Errors with like null values ?  I assumed not to fix those ? 
