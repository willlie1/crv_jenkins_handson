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
                // sh 'make check || true'
                junit '**/target/*.*'
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
                // sh 'make'
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
            }
        }
        stage('Deploy') {
                when {
                    expression {
                        currentBuild.result == null || currentBuild.result == 'SUCCESS' 
                    }
                }
            steps {
                echo 'Deploying....'
                // sh 'make publish'
            }            
        }
    }
}

