pipeline {
    agent any

    stages {
        stage('Clean') {
            steps {
                sh 'mvn clean'
                echo 'Cleaning..'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn install'
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn validate'
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