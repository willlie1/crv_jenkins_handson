pipeline {
    agent any

    stages {
        stage('Clean') {
            steps {
                echo 'Cleaning..'
                // mvn clean
                sh './mvnw clean'

            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                // sh 'make check || true'
                // junit '**/target/*.*'
                // mvn test
                sh './mvnw test'
        		junit '**/target/surefire-reports/*.xml'

            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
                // sh 'make'
                sh './mvnw compile'
                step $class: 'ArtifactArchiver', artifacts: '**/target/*.jar', fingerprint: true
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
            }            
        }
    }
}

