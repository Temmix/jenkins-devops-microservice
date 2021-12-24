pipeline {
	agent any
	// agent {  docker { image 'maven:3.6.3'} }
	// agent {  docker { image 'node:13.8'} }
	environment {
		dockerHome = tool 'MyDocker'
		mavenHome = tool 'MyMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage('Build') {
			steps {
				// sh 'node --version'
				sh 'mvn --version'
				sh 'docker --version'
				echo "Build"
				echo "PATH - $PATH"
				echo "BUILD NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_TAG - $env.BUILD_TAG"
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
