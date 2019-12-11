pipeline{
	agent any
	tools{
		maven 'Maven 3'
		jdk 'jdk1.8.0_211'
	}
	stages{
		stage('Compilation'){	
			steps{
			bat 'mvn compiler:compile'
			}
			
			
		}
stage('Test'){
			steps{
			bat 'mvn test'
			}
			post {
				always{
					junit 'target/surefire-reports/*.xml'
				}
			}
		}
	}
}
