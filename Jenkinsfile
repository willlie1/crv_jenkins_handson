node {
	checkout scm
	stage('clean') {
		sh './mvnw clean'
		echo 'cleaning'
	}
	stage('test') {
		sh './mvnw test'
		echo 'testing'
	}
	stage('build') {
		sh './mvnw package'
		echo 'building'
	}
	stage('deploy') {
		echo "Yay, we've deployed our application using a jenkins pipeline"
	}
}
