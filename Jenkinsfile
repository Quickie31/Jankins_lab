pipeline {
    agent {
        docker {
            image 'gcc:latest'
        }
    }
   
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Quickie31/Jankins_lab.git'
            }
        }
        stage('Build') {
            steps {
                sh 'g++ -o hello_world hello_world.cpp'
            }
        }
    }
   
    post {
        success {
            archiveArtifacts artifacts: 'hello_world', fingerprint: true
        }
    }
} 