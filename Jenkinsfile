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
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'make'
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'make check || true'
                junit '**/target/*.xml'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                when {
                  expression {
                    currentBuild.result == null || currentBuild.result == 'SUCCESS'
                  }
                }
                steps {
                    sh 'make publish'
                }
            }
        }
    }
}