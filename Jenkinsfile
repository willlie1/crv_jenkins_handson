pipeline {
    agent any

    stages {
        stage('Clean') {
            steps {
                sh 'echo clean'
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