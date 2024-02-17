pipeline {
    agent { label 'jenkins-agent' }
    
    tools {
        jdk 'Java17'
        maven 'Maven3'
    }
    
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
        
        stage("Build Application") {
            steps {
                sh "mvn clean package"
            }
        }
        
        stage("Test Application") {
           steps {
                 sh "mvn test"
            }
        }
    }
}
