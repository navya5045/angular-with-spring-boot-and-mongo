pipeline{
     agent any
        stages {
         stage('Build'){
           steps{
              echo 'Running build automation'
              sh './mavenw build --no-daemon'
              archiveArtifacts artifacts: 'demoApplication.zip' 
             
             }
         
          }
     }    
}
