pipeline {
   agent none

   environment {
        // Declare environment variables
        MY_VARIABLE = 'Hello, World!'
    }

    stages {
        stage('SAST') {
            steps {
                sh 'echo "SAST - Yet to be implemented"'
                // Access environment variables
                echo "My Variable: ${env.MY_VARIABLE}"                
            }
        }
        stage('Dependency Scan') {
            steps {
                sh 'echo "Dep Scan - Yet to be implemented"'
            }

        }        
        stage('Container Scan') {
            steps {
                sh 'echo "Container Scan - Yet to be implemented"'
            }
        }            
        stage('Docker Build and Push') {
            steps {
                script{
                    withCredentials([usernamePassword(credentialsId: 'dockerhub', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) {
                        cd app/express-js-app
                        docker build -t docker.io/333743/express-js-app:latest .
                        docker login -u ${USERNAME} -p ${PASSWORD}
                        docker push docker.io/333743/express-js-app:latest
                    }
                }
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Hello World Deploy stage."'
            }
        }
    }
}
