# Required Tools
* Docker
# Step By Step Guideline
1. ### Docker compose:
* Checkout the project from the Git link: https://github.com/MinhNguyenKh/Microservices-Docker-sample.git
* Open the terminal from _**docker-compose**_ directory then run the following commands in the order below:

	`docker-compose -f docker-compose-config.yml up`
	
	`docker-compose -f docker-compose-services.yml up`
	
	`docker-compose -f docker-compose-client.yml up`
	
	`docker-compose -f docker-compose-batch.yml up` ***this batch is only used to update data's status***
	
	Please note that it might take time to start up all the images in the _**docker-compose**_ file depending on machine as well as network. 
	
	Especially, for the _***docker-compose-client.yml***_ please wait until the keycloak server is ready to use:
	
	![image](https://user-images.githubusercontent.com/67884799/125185273-f038f580-e25e-11eb-8b5a-1d2f4142bf21.png)

2. ### Keycloak server configuration:

* Create _***User***_:

  Open browser then access the link: http://localhost:8080 then click on Administration Console and login with account _***minhnk/khanhminh***_ 

![image](https://user-images.githubusercontent.com/67884799/125399212-3d49d280-e3eb-11eb-9f0a-ceb975a23829.png)

After that choose ***Users*** tab to create your own user

You can fill whatever user's information you want in this section:

![image](https://user-images.githubusercontent.com/67884799/125185544-730e8000-e260-11eb-942f-92d295e768ae.png)

Then click on tab _***Credentials***_ and fill your password, turn of Temporary option then click ***Set Password***:

![image](https://user-images.githubusercontent.com/67884799/125185592-b0730d80-e260-11eb-9375-c5d5b6ba2110.png)

After that click on tab _***Roles Mapping***_ to assign role to your user
Choose ***angular-client*** in ***Client Roles*** and select ***ADMIN*** role if you select ***USER*** role, you can only see posts without creating permission.

![image](https://user-images.githubusercontent.com/67884799/125399627-d24ccb80-e3eb-11eb-9cc4-5e8475652e0a.png)

2. ### Access the project
* Open browser and access the link: http://localhost:4200 login with your own account which was created in previous step to use the project
