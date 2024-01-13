pipeline {
    agent {
        docker {
            image 'docker:20.10.16-dind '
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World Build stage."'
                sh 'docker info'
            }
        }
        stage('Test') {
            steps {
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
