node {
	  checkout scm

        stage ('Build'){
                echo 'Building..'
				sh './mvnw clean'
			}
			    stage('Test') {
        sh './mvnw test'
        junit '**/target/surefire-reports/*.xml'
    }
      }
