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
* Open browser then access the link: http://localhost:8080 and go to Admin Console page to create ***Realm***:

![image](https://user-images.githubusercontent.com/67884799/125185330-473eca80-e25f-11eb-8d1e-0b6c8b0a0529.png)

Please make sure that the name of Realm is the same as the image: ***demo-keycloak***

![image](https://user-images.githubusercontent.com/67884799/125185385-853bee80-e25f-11eb-928e-3ec4ef3f491a.png)

* Create _***Client***_: Go to _***Client***_ tab to create client:

![image](https://user-images.githubusercontent.com/67884799/125185460-df3cb400-e25f-11eb-81ea-bcd952f61f67.png)

Please make sure that the _***Client ID***_ and _***Root URL***_ are the same as the image below:

![image](https://user-images.githubusercontent.com/67884799/125185470-efed2a00-e25f-11eb-82da-80bb058c8c22.png)

* Create _***Client Role***_: After creating _***Client***_ click on _***Role***_ tab to create role for this client:

![image](https://user-images.githubusercontent.com/67884799/125185518-3f335a80-e260-11eb-84e9-8e01f0ede328.png)

![image](https://user-images.githubusercontent.com/67884799/125185521-45c1d200-e260-11eb-8d92-7273ed85e966.png)

Please make sure that the role name is the same as the image below:

![image](https://user-images.githubusercontent.com/67884799/125185523-4b1f1c80-e260-11eb-8f9b-ee02505b2748.png)

* Create _***User***_

You can fill whatever user's information you want in this section:

![image](https://user-images.githubusercontent.com/67884799/125185544-730e8000-e260-11eb-942f-92d295e768ae.png)

Then click on tab _***Credentials***_ and fill your password, turn of Temporary option then click ***Set Password***:

![image](https://user-images.githubusercontent.com/67884799/125185592-b0730d80-e260-11eb-9375-c5d5b6ba2110.png)

After that click on tab _***Roles Mapping***_ to assign role to your user
Choose ***angular-client*** in ***Client Roles*** and select the role that you created in the previous step

![image](https://user-images.githubusercontent.com/67884799/125185653-05168880-e261-11eb-8176-1e711a221b50.png)

2. ### Access the project
* Open browser and access the link: http://localhost:4200 to use the project
