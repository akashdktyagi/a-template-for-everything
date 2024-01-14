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
                        sh '''

                        cd apps/express-js-app
                        docker build -t docker.io/333743/express-js-app:latest .
                        docker login -u ${USERNAME} -p ${PASSWORD}
                        docker push docker.io/333743/express-js-app:latest

                        '''
                    }
                }
            }
        }

        stage('Deploy to Dev Namespace') {
            steps {
                sh '''
                   kubectl create deployment express-js-app --image=docker.io/333743/express-js-app:latest -n dev-ns -v=6
                   kubectl expose deployment express-js-app --type=NodePort --port=3000 -n dev-ns -v=6
                '''
            }
        }
    }
}
