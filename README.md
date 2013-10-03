Getting Started with App42PaaS-Grails-MongoDB Sample Application:
---------------------------------------------------------

This application is basically a simple User Input Form that takes input from user and saves it in database.

<b>[Download the source code from git.](https://github.com/shephertz/App42PaaS-Grails-MongoDB-Sample/archive/master.zip)</b>

Note: This project is build with grails 2.2.1 .


Using Grails with MongoDB:
-----------------------------

		1. Remove the hibernate dependency from the BuildConfig.groovy file. 
		 
		2. Add mongodb dependency in BuildConfig.groovy
				
				compile ":mongodb:1.3.0"
				
		    
		For further details on Grails-Mongo visit [http://blog.mongodb.org/post/18510469058/grails-in-the-land-of-mongodb](http://blog.mongodb.org/post/18510469058/grails-in-the-land-of-mongodb)
		
		

Project Configuration:
--------------------------
		 
        1. Open DataSource.groovy (located in grails-app/conf folder).

        2. Update the details of your MongoDB service in it.

                  grails { 
					mongo { 
						host = "your_service_host_url"
						port = your_service_port 
						username = "service_username"
						password="service_password"
						databaseName = "service_database_name"
					  } 
				  }

         3. Run the following command to create war: 
				
				grails war
					

Deploying Application on App42 PaaS using Binary:
---------------------------------------------------
					
		
	1. Run the app42 deploy command.
        
                  $ app42 deploy
                  $ Enter App Name: <your_app_name>
				  $ 1: Binary
				  $	2: Source
				  $ Choose Upload Type [Binary]: 1
                  $ Would you like to deploy from the current directory? [Yn]: n
                  $ Binary Deployment Path: <your_binary_path>
                  $ This process may take a while, be patient with it.
                  $ Deploying Application... OK
                  $ Please wait it may take few minutes.
                  $ Latest Status....|
                  $ App deployed successfully.
				  

Deploying Application on App42 PaaS using Source (Git):
--------------------------------------------------------

	1. Run the app42 deploy command.
	
				  $ app42 deploy
                  $ Enter App Name: <your_app_name>
				  $ 1: Binary
				  $	2: Source
				  $ Choose Upload Type [Binary]: 2
				  $ Enter Git URL?: <your_public_git_url>
				  $ Deploying Application... OK
                  $ Please wait it may take few minutes.
                  $ Latest Status....|
                  $ App deployed successfully.
