pipeline {
    agent any

    environment {
        version = sh script: './mvnw help:evaluate -Dexpression=project.version -q -DforceStdout', returnStdout: true
    }

    stages {
        stage('version check') {
            steps {
                echo "Version=${env.version}"
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
        stage('SNAPSHOT') {
            when {
                expression {
                    return env.version.contains("SNAPSHOT")
                }
            }
            steps {
                echo "This is a snapshot version we are not going to deploy anything"
            }
        }
        stage('RELEASE') {
            when {
                expression {
                    return !env.version.contains("SNAPSHOT")
                }
            }
            steps {
                echo "Yay, we've deployed our application using a jenkins pipeline"
            }
        }
    }
}
