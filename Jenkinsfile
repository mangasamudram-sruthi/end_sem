pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/mangasamudram-sruthi/end_sem.git'
            }
        }
        stage('Build and Deploy Containers') {
            steps {
                script {
                    sh 'docker-compose down'  // Stop any existing containers
                    sh 'docker-compose up -d' // Build and start the new containers
                }
            }
        }
    }
