// SCRIPTED

// DECLARATIVE
pipeline {
	agent any
	// agent {docker {image 'maven:3.6.3'}}

	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}

	stages {
		stage ('Build') {
			steps {
				sh 'mvc --version'
				sh 'docker version'
				echo 'Build'
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $PATH"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_URL - $env.BUILD_URL"

			}
		}
		stage ('Test') {
			steps {
				echo 'Test'
			}
		}
		stage ('Integration Test') {
			steps {
				echo 'Integration Test'
			}
		}
	} 
	post {
		always {
			echo "I am the Shaman!"
		}
		success {
			echo "I am a Success!"
		}
		failure {
			echo "He is a failure!"
		}
	}
}
