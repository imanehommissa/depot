pipeline{
	agent any
	tools{
		maven 'Maven 3'
		jdk 'jdk1.8.0_211'
	}
	stages{
		stage('build'){
				steps{
				bat 'mvn compiler:compile'
				}
				post {
                    success {
<<<<<<< HEAD
                     bat "echo 'Projet compilé avec succès'"
                    }
                    failure {
                     bat "echo 'Erreur lors de la compilation du projet'"
=======
                     bat "echo 'Projet compilé avec succès'"     
                    }
                    failure {
                     bat "echo 'Erreur lors de la compilation du projet'"     
>>>>>>> cd04846ef6b46fd36c0d6ab1e4bebe1fa918ab44
                    }
              }
		}
		stage('Test') {
            steps {
                bat 'mvn test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
		stage('couverture') {
            steps {
<<<<<<< HEAD

                bat 'mvn cobertura:cobertura -Dcobertura.report.format=xml'

=======
               
                bat 'mvn cobertura:cobertura -Dcobertura.report.format=xml'
                
>>>>>>> cd04846ef6b46fd36c0d6ab1e4bebe1fa918ab44
            }
             post {
                  always {
                        cobertura coberturaReportFile: '**/target/site/cobertura/coverage.xml'
<<<<<<< HEAD

=======
                       
>>>>>>> cd04846ef6b46fd36c0d6ab1e4bebe1fa918ab44
                        }
                  }
        }
	}
}
