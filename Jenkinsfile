pipeline {
    agent any
    
    stages {
        stage('Git checkout') {
           steps{
                git branch: 'main', url: 'https://github.com/vangimallaMahesh/git-jenkins-terraform-ec2.git'
            }
        }
        stage('terraform format check') {
            steps{
                sh 'terraform fmt'
            }
        }
        stage('terraform Init') {
            steps{
                sh 'terraform init'
            }
        }
        stage('terraform apply') {
            steps{
                sh 'terraform apply --auto-approve'
            }
        }
    }

    
}

    
