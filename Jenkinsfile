pipeline {
agent any
    tools {
        maven 'Maven 4.0.0'
        jdk 'jdk8'
    }
    stages {
        stage('Clean') {
            steps {
                echo 'Cleaning..'
                sh './mvnw clean'
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
                sh './mvnw package'
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh './mvnw test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}