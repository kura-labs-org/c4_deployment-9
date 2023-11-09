<p align="center">
<img src="https://github.com/kura-labs-org/kuralabs_deployment_1/blob/main/Kuralogo.png">
</p>

## Group Instructions:
1. **Everyone is responsible for submitting the main repository link and updating the main repository**  
2. Each person in a group must pick one role from below:
```
Project Manager:
- Make sure everyone is working on their part of the deployment
- Manage the time for each deliverable
- Create the main deployment repo in GitHub (and invite team members to it)
- Create a Jira board (and invite team members to it)
- Work on creating both Jenkinsfile with other members

Chief Architect:
- Create the deployment diagram
- Create the Terraform files
- Work on creating both Jenkinsfile with other members

System Administrator:
- Create the Docker container images for ECS 
- Create AWS user accounts for each member of your group to access your account with
- Work on creating both Jenkinsfile with other members

```
3. Here are your groups:
```
Group 1: Danielle, Kevin G, Jo
Group 2: Aubrey, Nehemiah, Darrielle
Group 3: Annie, Jorge, Sameen
Group 4: Ethan, Khalil, Luis
Group 5: Dwayne, Saraswati, Andrew
Group 6: Nalani, Kevin E
Group 7: Brittney, Dolma, Belinda

```

*********************************************************************************************************************************************************************
## Deployment Instructions:

1. Create a Python script that will email the team when the pipline is done or send an SMS to your team via Twilio 
2. Create a Jenkins manager and agent architecture:
```
Instance 1:
- Jenkins, Docker pipeline plugin
Instance 2 (T.2 medium):
- Docker and default-jre 
Instance 3 (T.2 medium):
- Kubectl, EKS and default-jre (Install your cluster and add the loadbalancer)
```
3. Create a VPC with the following components:
    - 2 Public subnets
    - 2 Private subnets
    - Internet Gateway
    - Nat Gateway  
4. Create a deployment and services manifest for the E-commerce application:
    - Create a service and deployment for the backend
    - Create a service and deployment for the frontend     
6. Make sure your cluster is created and the Jenkins agent is connected to the cluster
7. Use your Docker image of the Backend from Deployment 8
8. Create the frontend image but place the selector:app:name into the package.json file
9. Now deploy the EKS files with Jenkins


