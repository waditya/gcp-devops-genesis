## Sprint-04

Goals of the Sprint - 

1. Understand Cloud Builds in detail
2. How to connect Cloud Build to GitHub repository
4. Implementing automation to build the docker image and store it in artifactory after code merge.

### Understanding Cloud Build

| Feature | Details |
| ---     | -----   |
| 1       | Build Software quickly across all programming languages, including Java, Go, Node.js and more | 
| 2       | Choose build machines from 15 machines types and run many concurrent buils per pool           |
| 3       | Post build , depploy the image across multiple environments such as VMs, serverless, Kubernetes, or Firebase | 
| 4       | Access cloud-based, fully managed CI/CD workflows within your private network | 
| 5       | Keep your data at rest within a geographical region or specific location with data residency |

### Takeaways

1. Cloud build is a complete serverless CI/CD platform
2. No infrastructure to maintain
3. Pricing : E2 - Medium serverless $0.003 per build/minute
4. Code: Written in YAML file 
   Example - Unlike CloudBuild, a user of Jenkin will have to write the deployment logic in Groovy script.

### Connecting Cloud Build to GitHub

1. Use Cloud Build Trigger to connect GitHub and Cloud Build
2. Trigger is an event which will start the Cloud Build branch
3. Any push on the main branch will trigger Cloud Build
4. Cloudbuild.yaml file shall contain the Continuous Deployment (CD) Code