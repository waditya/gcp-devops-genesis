## Sprint-03

1. Design discussion on CICD
2. Code in GitHub repo needs to be deployed on GCP GKE cluster
3. Questions around the GKE process - 
 - i. How do we automate the way to build the docker image
 - ii. How do we store the docker image in an artifactory 
     a. Public alternative - DockerHub (not useful for private companies)
 - iii. Write code (YAML files for deployment and service ) to deploy the artifactory image on GKE
 - iv. We may also need YAML files for Horizontal Pod autoscaling and Ingress
 - v. We have to setup CD to deploy this code to GKE using the docker image in the artifactory.

 4. Summarizing the above questions - 
   a. Automate way to build the docker image
   b. Store the docker image in an artifactory
   c. Write manifest files for deployment , service and/or ingress and horizontal pod autoscaler
   d. Setup CD to deploy the code to GKE using the docker image stored in artifactory.

5. What tools in GCP can help us achieve task#4 

| Task | GCP Service |
| : ---------------------------------------------------- | :-----------: |
| Automate way to build the docker image from Git code | Cloud Build |
| Storing the image | GCP Artifact Registry | 
| Deploy to GKE cluster | Cloud Build |  

6. Tasks for next Sprint
   i. Build and Store Docker Image
   ii. Deploy Docker image to GKE

