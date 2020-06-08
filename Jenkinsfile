pipeline {
    agent any

    stages {
        stage('Clean') {
            steps {
                mvn clean
                echo 'Cleaning..'
            }
        }
        stage('Build') {
            steps {
                mvn install
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                mvn validate
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