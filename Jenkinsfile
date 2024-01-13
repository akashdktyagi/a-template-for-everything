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
