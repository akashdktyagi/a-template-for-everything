# A template for Everything
### As name suggests I intend to elabolate and implement almost all the important aspects of Software Engineering in this repository.
#### Dev Sec Ops, CI CD, Security tools, Testing Tools
#### Some Architecture Patterns: API Gateway, Asysnc and Streaming with kafka
#### Infra: K8s, terraform

* CI CD: Set up Jenkins with Bintami Jenkins Image on AWS 
    * Basic Jenkins Set Up: https://progress-bar.dev/100/?title='Basic Jenkins Set Up'
    * Pipeline Creation: https://progress-bar.dev/58/?title=Pipeline Creation
* Deployment with K8s: Set up a Microk8s server on EC2 instance for app deployment during Pull Request as well as final deployment
* App development: with Express.js, Flask API and Java Spring Boot
    * Expres JS Simple App
    * A flask API for the Front end
    * Set Java Spring Boot APIs for Kafka and other things
* API Gateway: Spring Cloud APi Gateway
* Security and Testing:
    * Unit test
    * Sonar Integration for SAST
    * Dep Scan
    * Container Scan with Trivy
    * Application test with Selenium and other
    * Perf Test
    * DAST test
* Deployment Strategy:
    * Blue Green
    * Canaray
* Monitoring with Prometheus and Grafana
* Infra as Code with Terraform

Lets start:

1. Set up Jenkins server on AWS. [Step 1 Jenkins Set Up on AWS EC2](jenkins/step1-jenkins-setup.md)
2. Create the Project [Step 2 Jenkins Create Project](jenkins/step2-jenkins-create-project.md)
3. Create an express JS App [Create an Express JS App](apps/express-js-app/README.md)
4. Set up micro k8s server [Set Up a Microk8s app](microk8s/step-3-microk8s-setup.md)

