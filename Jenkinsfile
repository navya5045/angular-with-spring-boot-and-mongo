pipeline {
    agent any
    
    tools {
        // Install the Maven version configured as "MMAVEN" and add it to the path.
        maven "MAVEN"
    }

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/navya5045/angular-with-spring-boot-and-mongo'

                // Run Maven on a Unix agent.
                sh "mvn -Dmaven.test.skip=true clean package"

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }

            post {
                // If Maven was able to run the tests, even if some of the test
                // failed, record the test results and archive the jar file.
                success {
                    
                    archiveArtifacts 'target/*.jar'
                }
            }
        }
    }
}
