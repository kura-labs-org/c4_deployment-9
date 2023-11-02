<p align="center">
<img src="https://github.com/kura-labs-org/kuralabs_deployment_1/blob/main/Kuralogo.png">
</p>

## Group Instructions:
1. **Everyone is responsible for submitting the main repository link and updating the main repository**  
2. Here are your group roles:
```
Role Manager:
- This role is responsible for making sure everyone is working on their part of the deployment, managing the time for each deliverable, and this role is responsible for the main repository.
- Also, creating a Jira board and inviting team members to it

Chief Architect:
- This role is responsible for the creation of the diagram and creating the Terraform files.

System Administrator:
- This role is responsible for the creation of the container images and ECS.

```
3. Here are your groups:
```
Group 1:
- Danielle, Kevin G, Joeseph
Group 2:
- Aubrey, Nehemiah, Darrielle
Group 3:
- Annie, Jorge, Sameen
Group 4:
- Kevin E, Belinda, Ethan
Group 5:
- Dwayne, Saraswati, Andrew
Group 6:
- Khalil, Luis, Nalani
Group 7:
- Brittney, Dolma

```

*********************************************************************************************************************************************************************
## Deployment Instructions:

1. Create a Jenkins manager and agent architecture:
```
Instance 1:
- Jenkins, Docker pipeline plugin
Instance 2 (T.2 medium):
- Docker and default-jre 
Instance 3:
- Terraform and default-jre
```
2. Create an ECS and VPC Terraform file with the following components listed below:
    - 2 AZ's
    - 2 Public Subnets
    - 2 Containers for the frontend
    - 1 Container for the backend
    - 1 Route Table
    - Security Group Ports: 8000, 3000 and 22
    - 1 ALB    
3. Create a Docker image of the Backend on a T.2 medium:
```
Follow these steps
- sudo apt install -y software-properties-common
- sudo add-apt-repository -y ppa:deadsnakes/ppa
- sudo apt install python3.9-venv
- git clone {Your repo}
- cd backend
- python manage.py migrate
- python manage.py runserver 0.0.0.0:8000
```
4. Create a Docker image of the frontend on a T.2 medium:
```
Follow these steps
- curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
- export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")" [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
- nvm install 10
- git clone {Your repo}
- cd frontend
- npm install
- npm start
```
5. Deploy the backend first, once it's deployed, copy the private IP address  
6. Place the private address in the pacakage.json file. Replace the current IP on line 4 to your private IP
7. Deploy the frontend
8. Check your infrastructures and applications
9. What is the application stack of this application?
10. Is the backend an API server?  

