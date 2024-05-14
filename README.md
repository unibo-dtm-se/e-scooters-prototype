Software Engineering @ DTM | EIT Digital - a.y. 2023-2024 

# E-Scooters Case Study - Proof-of-Concept Prototype

v.1.0.0-20240513

## Organisation

Three microservices on the backend side:  

- **account-service**   
- **escooter-service**  
- **renting-service**  

Two frontends for users and the e-scooter company:  
 
- **user-app**  
- **company-dashboard**  

Embedded software on e-scooters:

- **escooter-agent-simple**

## Description

### account-service

- Microservice for managing the set of user accounts
- Running on port 5050

### escooter-service

- Microservice for managing the set of e-scooters device 
- Running on port 5060

### renting-service

- Microservice for managing the rents
- Running on port 5070

### company-dashboard

- Web-based dashboard showing the position of e-scooters
- Based on a backend running on port 5200

### user-app

- Web-based app for users to subscribe to the service
- Based on a backend running on port 5300

### escooter-agent-simple

- Software Agent controlling an e-scooter (emulating embedded software)
- Running on port 5100 
 
## (Manual) **Deployment** ##

- To clone the repository
	- Open a terminal
	- change dir to the directory where to store and run the demo
	- type: ``git clone https://github.com/unibo-dtm-se/e-scooters-prototype.git``  
	
	You should see a new directory ``e-scooters-prototype``, including a subdirectory for each subsystem: ``account-service``, ``e-scooter-service``, ``renting-service``, ``user-app``,``company-dashboard``,``escooter-agent-simple``


- To run the **account-service**:  
	- Open a terminal
	- change dir to ``account-service`` directory
	- to install libraries first type: ``npm install``
	- to run the service type: ``npm start`` 

	You should see: ``Account service up and running - listening on port 5050``

- To run the **e-scooter-service**:  
	- Open a terminal
	- change dir to ``escooter-service`` directory 
	- to install libraries first type: ``npm install``
	- to run the service type: ``npm start``

	You should see: ``E-Scooter service up and running - listening on port 5060``

- To run the **renting-service**:
	- Open a terminal
	- change dir to ``renting-service`` directory 
	- to install libraries first type: ``npm install``
	- to run the service type: ``npm start``

	You should see: ``Renting service up and running - listening on port 5070``

- To run the **user-app**
	- Open a terminal
	- change dir to ``user-app`` directory  
	- to install libraries first type: ``npm install``
	- to run the web app backend type: ``npm start``

	You should see: ``User app backend un and running at 5300``

	To see the user app in action to register a new user, open the browswer and go to:  
	
	``http://localhost:5300/registration.html``  
	
	(try with a not existing user and with an existing user)


- To run the **company-dashboard**
	- Open a terminal
	- change dir to ``company-dashboard`` directory
	- to install libraries first type: ``npm install``
	- to run the web app backend type: ``npm start``

	You should see:``Company dashboard endpoint at 5200``

	To see the dashboard, open a new browser window and go to:
	
	``http://localhost:5200/escooters-dashboard.html``

	You should see a map (Cesena Campus)

- To run the simple **e-scooter controlling agent**
	- Open a terminal  
	- change dir to ``escooter-agent-simple`` directory
	- to install libraries first type: ``npm install``
	- to run the agent type: ``npm start``

For the demo we use the [Postman application](https://www.postman.com/) to directly interact with services, reproducing some use cases.  After running the application, upload the collection ``API-postman_collection.json`` available in the repo root.  The collection includes main API that can be used to emulate the case study.

Proposed demo -- sequence of requests (included in the collection API) to be done:

- get current users
- add a new user
- get again the list of users
- add an escooter
- get the list of escooters
- get the state of an escooter
- start a new rent
- get the rent info
- configure the agent to control the escooter
- turn the scooter on
- activate automode
(check the map)
- deactivate automode
- turn the scooter off
- end the rent 


## (Automated) **Deployment** ##

Docker can be used to automate the deployment. A full CI Environment  can be used to automate all the process.
