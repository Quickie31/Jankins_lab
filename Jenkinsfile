pipeline {
    agent {
        docker {
            image 'gcc:latest'
        }
    }
   
    stages {
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
