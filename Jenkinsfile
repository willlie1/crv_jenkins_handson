pipeline {
	agent any

	stages {
		stage('clean') {
			steps {			
				echo 'cleaning project'
			}
		
		}
		stage('test') {
			steps {			
				echo 'testing code'	
			}
		}
		stage('build') {
			steps {
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
