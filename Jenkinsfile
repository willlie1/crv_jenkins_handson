pipeline {
    agent any

    stages {
        stage('Clean') {
            steps {
                echo ‘Cleaning..’
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'make check || true'
                junit '**/target/*.xml'
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

