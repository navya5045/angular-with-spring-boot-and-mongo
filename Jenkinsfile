pipeline {
    agent any
    
    tools {
        
        maven "MAVEN"
    }

    stages {
         stage('package') {
             steps {
                
                git 'https://github.com/navya5045/angular-with-spring-boot-and-mongo'
               
                sh "mvn clean compile"

               
            }
        }

        stage('package') {
            steps {
                
                git 'https://github.com/navya5045/angular-with-spring-boot-and-mongo'
               
                sh "mvn -Dmaven.test.skip=true clean package"

               
            }

            post {
                
                success {
                    
                    archiveArtifacts 'target/*.jar'
                }
            }
        }
    }
}
