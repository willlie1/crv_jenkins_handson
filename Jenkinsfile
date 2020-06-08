node {
    checkout scm
    
    stage('Clean') {
        echo 'Cleaning....'
        sh './mvnw clean'
    }
    stage('Test') {
        echo 'Testing....'
        sh './mvnw test'
        junit '**/target/surefire-reports/*.xml'
    }
    stage('Build') {
        echo 'Building....'
        sh './mvnw package -Dmaven.test.skip'
        step $class: 'ArtifactArchiver', artifacts: '**/target/*.jar', fingerprint: true
    }
    stage('Deploy') {
        echo 'Deploying....'
    }
}