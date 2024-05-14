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
 
