pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    // Build Docker image using Dockerfile
                    def dockerImage = docker.build('my-spring-boot-app', '.')
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    // Run Docker container based on the built image
                    def dockerContainer = docker.image('my-spring-boot-app').run('-p 4050:4050')
                }
            }
        }

        stage('Test') {
            steps {
                echo 'No tests are currently implemented'
            }
        }
    }
}
