pipeline {
    agent any

    stages {
        stage('clean') {
            steps {
                sh './mvnw clean'
            }
        }
        stage('Test') {
            steps {
                sh './mvnw test'
                junit '**/target/surefire-reports/*.xml'
            }
        }
        stage('Build') {
            steps {
                // no need to test again, so -Dmaven.test.skip
                sh './mvnw package -Dmaven.test.skip'
                // Adding artifact to archive
                step $class: 'ArtifactArchiver', artifacts: '**/target/*.jar', fingerprint: true
            }

        }
        stage('Deploy') {
            steps {
                echo "Yay, we've deployed our application using a jenkins pipeline"
            }
        }
    }
}