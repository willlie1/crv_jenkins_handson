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
        sh './mvnw package -Dmaven.test.skip'
        step $class: 'ArtifactArchiver', artifacts: '**/target/*.jar', fingerprint: true
    }
    stage('Deploy') {
        echo "Yay, we've deployed our application using a jenkins pipeline"
    }
}