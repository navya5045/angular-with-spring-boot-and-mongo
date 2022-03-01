pipeline{
     agent any
        stages {
         stage('Build'){
           steps{
              echo 'Running build automation'
       
              archiveArtifacts artifacts: 'demo-0.0.1-SNAPSHOT.jar' 
             
             }
         
          }
     }    
}
