pipeline {
    agent { label 'jenkins-agent' }
            
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
