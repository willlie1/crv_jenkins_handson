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
        stage('Test') {
            steps {
                echo 'Testing..'
                sh './mvnw test'
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
