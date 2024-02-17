pipeline {
    agent { label 'jenkins-agent' }
         tools{
             maven 'Maven3'
         }
        stages{
        stage("Cleanup Workspace"){
                steps {
                cleanWs()
                }
        }
        
        stage("Build Application"){
            steps {
                sh "mvn clean package"
            }

       }

       stage("Test Application"){
           steps {
                 sh "mvn test"
           }
       }
      
        }     
 
}
