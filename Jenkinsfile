pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/nguyenvancongdev/hello-nodejs.git'
            }
        }
        stage('Build stage') {
            steps {
                
               withDockerRegistry(credentialsId: 'docker-hub', url: 'https://index.docker.io/v1') {
                   sh 'docker build -t nguyenvancongdev/automation_IOPS .'
                //    sh 'docker push nguyenvancongdev/automation_IOPS'
                }
            }
        }
    }
}