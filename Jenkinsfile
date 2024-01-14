pipeline {
   agent any

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
                        sh "cd apps/express-js-app"
                        sh "docker build -t docker.io/333743/express-js-app:latest ."
                        sh "docker login -u ${USERNAME} -p ${PASSWORD}"
                        sh "docker push docker.io/333743/express-js-app:latest"
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
