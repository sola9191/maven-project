pipeline {
    agent any
	
    tools {
        maven 'Apache Maven 3.8.1'
    }
    stages {
	stage('Build'){
		steps{
		   sh 'mvn clean package'
		}
	}
    }
}
