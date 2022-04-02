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
                sh 'docker -v'
               withDockerRegistry(credentialsId: 'docker-hub1', url: 'https://index.docker.io/v1') {
                //    sh 'docker build -t nguyenvancongdev/automation_IOPS .'
                //    sh 'docker push nguyenvancongdev/automation_IOPS'
                }
            }
        }
    }
}