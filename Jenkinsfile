pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                // Clone repository từ GitHub
                git branch: 'main', url: 'https://github.com/22120137/22120137.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                // Xây dựng Docker image
                script {
                    docker.build('22120137_app')
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                // Chạy Docker container
                script {
                    docker.image('22120137_app').run()
                }
            }
        }
    }
}
