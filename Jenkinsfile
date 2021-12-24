pipeline {
	// agent any
	agent { docker { image 'maven:3.6.3'} }
	stages {
		stage('Build') {
			steps {
				sh 'mvn --version'
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
