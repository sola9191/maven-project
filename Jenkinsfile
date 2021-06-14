pipeline {
    agent any
	
    tools {
        maven 'Apache Maven 3.8.1'
    }

    stages{
        stage('Build'){
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
	stage ('Deploy to Staging'){
            steps {
                build job: 'Deploy-to-staging'
            }
        }
    }
}
