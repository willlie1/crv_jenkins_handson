pipeline {
    agent any

    stages {
        stage('Clean') {
            steps {
                sh './mvnw clean'
                echo 'Cleaning..'
            }
        }
        stage('Build') {
            steps {
                sh './mvnw install'
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                sh './mvnw validate'
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