node {
    stage('clean') {
        steps {
            sh ./mvnw clean
        }
    }
    stage('test') {
        steps {
            sh ./mvnw test
        }
    }
    stage('build') {
        steps {
            sh ./mvnw isntall
        }
    }
    stage('deploy') {
        echo "Yay, we've deployed our application using a jenkins pipeline"
    }
}