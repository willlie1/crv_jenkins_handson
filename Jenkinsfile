pipeline {
	agent any

	stages {
		stage('clean') {
			steps {			
				sh './mvnw clean'
				echo 'cleaning project'
			}
		
		}
		stage('test') {
			steps {			
				sh './mvnw test'
				echo 'testing code'	
			}
		}
		stage('build') {
			steps {
				sh './mvnw package'
				echo 'building source code'
			}
		}
		stage('deploy') {
			steps {
				echo "Yay, we've deployed our application using a jenkins pipeline"
			}
		}

	}
}
