pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				echo "Build"
			} 
		}
		stage('Test') {
			steps {
				echo "Test"
			} 
		}
		stage('Integration Test') {
			steps {
				echo "Integration Test"
			} 
		}
	} 
	post {
		always {
			echo 'I am always running :)'
		}
		success {
			echo 'I am awesome, success all the way :)'
		}
		failure {
			echo 'oooOps, something went wrong :('
		}
	}
}
