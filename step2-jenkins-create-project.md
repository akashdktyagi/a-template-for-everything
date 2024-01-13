### 2. Jenkins Create project

* Click new item and select pipeline project
* ![Alt text](ss/image-1.png)
* Below credentials will only be needed if your project is private if it is public then no need for credentials. Skip to the configure project.
* Create a github token from github account and add the token in jenkins credentials manager.
![Alt text](ss/image-2.png)
![Alt text](ss/image-3.png)
![Alt text](ss/image-4.png)
* Add github credentials in Jenkins Credentials manager: 
![Alt text](ss/image-5.png)

* Configure the project as per below screenshot:
![Alt text](ss/image-6.png)

* Project expect a Jenkinsfile in the root directory of the project. Lets add that with below code snippet and check in the code. After checkin the code run the pipeline.

```
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World Build stage."'
                sh 'docker info'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Hello World Test stage."'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Hello World Deploy stage."'
            }
        }
    }
}

```

![Alt text](ss/image-7.png)

* Click on the Console Output
![Alt text](ss/image-8.png)


