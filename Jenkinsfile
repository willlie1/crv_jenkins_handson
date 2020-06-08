pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
				sh './mvnw install'
				}
      }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}