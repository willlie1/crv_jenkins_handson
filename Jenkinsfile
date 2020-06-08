pipeline {
    agent any

    stages {
        stage('clean'){
	  steps{
	    echo 'Cleaning..'
            // mvn clean
            sh './mvnw clean'
          }
        }
        stage('Build') {
            steps {
                echo 'Building..'
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
