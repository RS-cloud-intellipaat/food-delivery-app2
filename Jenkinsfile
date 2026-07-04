pipeline {
    agent { label 'build-agent' }

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t food-delivery-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh '''
                docker rm -f food-app || true
                docker run -d --name food-app -p 8081:80 food-delivery-app
                '''
            }
        }
    }
}
