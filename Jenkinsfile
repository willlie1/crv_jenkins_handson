node {
    checkout scm

    stage('clean') {
        sh './mvnw clean'
    }
    stage('Test') {
        sh './mvnw test'
        junit '**/target/surefire-reports/*.xml'
    }
    stage('Build') {
        // no need to test again, so -Dmaven.test.skip
        sh './mvnw package -Dmaven.test.skip'

        // Adding artifact to archive
        step $class: 'ArtifactArchiver', artifacts: '**/target/*.jar', fingerprint: true
    }
    stage('Deploy') {
        echo "Yay, we've deployed our application using a jenkins pipeline"
    }
}