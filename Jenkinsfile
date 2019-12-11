pipeline{
	agent any
	tools{
		maven 'Maven 3'
		jdk 'jdk1.8.0_211'
	}
	stages{
		stage('Build'){	
			steps{
			bat 'mvn install'
			}
			post {
				success{
					junit 'target/surefire-reports/**/*.xml'
				}
			}
		}
        stage('Test'){	
			steps{
			bat 'mvn test'
			}
			post {
				success{
					junit 'target/surefire-reports/*.xml'
				}
			}
		}
	}
}
