pipeline {
    agent { label 'jenkins-agent' }
    
    
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                // sh 'sudo apt update'
                //sh 'sudo apt upgrade'
                //sh 'sudo apt install temurin-17-jdk'
                //sh 'touch /home/ubuntu/Jenkins-build-"${BUILD_NUMBER}"'
            }
        }   
        
        stage('CLeanup Workspace') {
            steps {
                cleanWs()
            }
        }
        
        stage('Checkout SCM') {
            steps {
                 git branch: 'main', credentialsId: 'github', url: 'https://github.com/alwaystilted/register-app'
            }
        }
        
      
        }
 
}
