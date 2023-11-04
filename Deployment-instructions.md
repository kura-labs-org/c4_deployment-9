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

1. Create a Python script that will automatically push to Github but check all files in the current directory for sensitive information such as AWS secret keys and AWS access keys and will return back to the terminal a message saying what document the sensitive information is in and what the sensitive information is. Also, it stops the script from being pushed to GitHub
2.  Create a Jenkins manager and agent architecture:
```
Instance 1:
- Jenkins, Docker pipeline plugin
Instance 2 (T.2 medium):
- Docker and default-jre 
Instance 3:
- Terraform and default-jre
```
3. Create an ECS and VPC Terraform file with the following components listed below:
    - 2 AZ's
    - 2 Public Subnets
    - 2 Containers for the frontend
    - 1 Container for the backend
    - 1 Route Table
    - Security Group Ports: 8000, 3000, 80 
    - 1 ALB    
4. Create a Docker image of the Backend on a T.2 medium:
```
Follow these steps
- Python 3.9 required 
- git clone {Your repo}
- cd backend
- install requirements.txt
- python manage.py migrate
- python manage.py runserver 0.0.0.0:8000
```
5. Create a Docker image of the frontend on a T.2 medium (The frontend runs on port 3000):
```
Follow these steps
- node 10 required
- git clone {Your repo}
- cd frontend
- npm install
- npm start
```
6. Create a Jenkinsfile to deploy the backend ECS Terraform files first, once it's deployed, copy the private IP address from the ECS console  
7. Place the private address in the pacakage.json file. Replace the current IP on line 4 to your private IP
8. Create another Jenkinsfile to deploy the ECS Terraform frontend files
9. Check your infrastructures and applications
10. What is the application stack of this application?
11. Is the backend an API server?  

