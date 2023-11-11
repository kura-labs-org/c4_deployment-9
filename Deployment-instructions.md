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
- Create the Docker container images for EKS
- Create the Kubernetes manifest
- Create AWS user accounts for each member of your group to access your account with
- Work on creating both Jenkinsfile with other members

Data Engineer:
- ?

```
3. Here are your groups and roles:
```
1. Aubrey- Data, Nehemiah- Manager, Darrielle- Chief Architect, Jo- System Admin, Nalani- System Admin
2. Annie- Data, Jorge- Manager, Sameen- Chief Architect, Kevin E- System Admin
3. Ethan- Manager, Khalil- Data, Luis- System Admin, Danielle- Chief Architect
4. Dwayne- System Admin, Saraswati- Data, Andrew- Manager, Kevin G- Chief Architect
5. Brittney-System Admin, Dolma- Manager, Belinda- Chief Architect

```

*********************************************************************************************************************************************************************
## Deployment Instructions:

1. Create a Python script that will email the team when the pipeline is done
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
6. Make sure your cluster is created and the instance 3 is connected to the cluster
7. Create your ALB controller: [instructions here](https://docs.google.com/document/d/1Y_c_ByV8y9I1CL8NJvZLqo6ftahcJJD5qG0WA_PkqTM/edit?usp=sharing)
8. Use your Docker image of the Backend from Deployment 8
9. Create the frontend image and place the service name into the package.json file
10. Now have Jenkins create the docker image and deploy to EKS
11. [Install Cloudwatch Agent on AWS EKS](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Container-Insights-setup-EKS-addon.html)


