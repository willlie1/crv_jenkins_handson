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
                sh 'echo install'
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                sh 'echo validate'
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