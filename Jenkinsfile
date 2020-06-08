def version = sh script: './mvnw help:evaluate -Dexpression=project.version -q -DforceStdout', returnStdout: true

pipeline {
    agent any

    stages {

        stage('version check') {
            steps {
                echo "version ${version}"
            }
        }

        stage('clean') {
            steps {
                sh './mvnw clean'
            }
        }
        stage('test') {
            steps {
                sh './mvnw test'
                junit '**/target/surefire-reports/*.xml'
            }
        }
        stage('build') {
            steps {
                sh './mvnw package -Dmaven.test.skip'
                step $class: 'ArtifactArchiver', artifacts: '**/target/*.jar', fingerprint: true
            }
        }
        stage('deploy') {
            steps {
                echo "Yay, we've deployed our application using a jenkins pipeline"
            }
        }
    }

}