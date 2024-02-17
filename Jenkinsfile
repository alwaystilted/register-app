pipeline {
    agent { label 'jenkins-agent' }
            
        stage('CLeanup Workspace') {
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
