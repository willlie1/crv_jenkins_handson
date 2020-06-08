
node {
    checkout scm

    stage('Clean') {
        sh './mvnw clean'
    }
    stage('Build') {
        sh './mvnw install -Dmaven.test.skip'

        // Adding artifact to archive
        //step $class: 'ArtifactArchiver', artifacts: '**/target/*.jar', fingerprint: true
    }
    stage('Test') {
        sh './mvnw test'
    }
    stage('Deploy') {
        echo 'Deploying....'
    }
}

// pipeline {
//     agent any
//
//     stages {
//         stage('Clean') {
//             steps {
//                 sh './mvnw clean'
//                 echo 'Cleaning..'
//             }
//         }
//         stage('Build') {
//             steps {
//                 sh './mvnw install'
//                 echo 'Building..'
//             }
//         }
//         stage('Test') {
//             steps {
//                 sh './mvnw validate'
//                 echo 'Testing..'
//             }
//         }
//         stage('Deploy') {
//             steps {
//                 echo 'Deploying....'
//             }
//         }
//     }
// }