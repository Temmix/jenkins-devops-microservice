pipeline {
	agent any
	// agent {  docker { image 'maven:3.6.3'} }
	// agent {  docker { image 'node:13.8'} }
	stages {
		stage('Build') {
			steps {
				// sh 'node --version'
				// sh 'mvn --version'
				echo "Build"
				echo "PATH - $PATH"
				echo "BUILD NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_URL - $env.BUILD_URL"
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
