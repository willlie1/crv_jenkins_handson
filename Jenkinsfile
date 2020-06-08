
//Declarative Pipeline
pipeline {
    agent any

    stages {
        stage('Clean') {
            steps {
                echo 'Cleaning..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
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