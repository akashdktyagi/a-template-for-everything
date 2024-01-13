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
            docker.image('maven:3.3.3-jdk-8').inside {
                sh 'echo "Hello World Test stage from inside Docker."'
                sh 'mvn -B clean install'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Hello World Deploy stage."'
            }
        }
    }
}
