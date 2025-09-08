**EKS Blue/Green Deployment with Jenkins**
**Prerequisites**
•	Terraform installed
•	Java 8 installed
•	kubectl installed
•	Docker installed
Steps
1.	**Full Setup**
Below actions are performed
2.	Create the EKS cluster with Terraform
3.	Deploy Jenkins to Kubernetes
4.	Build & push initial Blue and Green images
5.	Deploy Blue & Green deployments
6.	Point service to Blue initially
**2. CI-CD**
Jenkins job to automatically update deployment and switchover. Below is the flow:
Two identical environments:
Blue: live (serving users)

Green: idle (ready for updates)
On each deployment:
Detects which version is live

Deploys new code to the idle version

Switches service traffic to idle version (making it live)

Keeps the old live version running for instant rollback

