
//Declarative Pipeline
pipeline {
    agent any

    stages {
        stage('Clean') {
            steps {
                echo 'Cleaning..'
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
                sh './mvnw package'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}

//Scripted Pipeline
node {
    stage('Clean') {
        echo 'Cleaning....'
    }
    stage('Test') {
        echo 'Testing....'
    }
    stage('Build') {
        echo 'Building....'
    }
    stage('Deploy') {
        echo 'Deploying....'
    }
}