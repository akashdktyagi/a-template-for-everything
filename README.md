# Jenkins Reference Pipeline
#### This Repository holds the demonstration of an ideal Jenkins Pipeline. I intend to show below thigs:

* Set up Jenkins with Bintami Jenkins Image on AWS
* Set up a Microk8s server on EC2 instance for app deployment during Pull Request as well as final deployment
* App development with Express.js
* Unit test
* Sonar Integration for SAST
* Dep Scan
* Container Scan with Trivy
* App test
* Perf Test
* DAST test
* Deployment from One Env to other Env in continuity

Lets start:

1. Set up Jenkins server on AWS. [Step 1 Jenkins Set Up on AWS EC2](step1-jenkins-setup.md)
2. Create the Project [Step 2 Jenkins Create Project](step2-jenkins-create-project.md)
3. Create an express JS App [Create an Express JS App](apps/express-js-app/README.md)
4. Set up micro k8s server [Set Up a Microk8s app](step2-jenkins-create-project.md)

