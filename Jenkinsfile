// SCRIPTED

// DECLARATIVE
pipeline {
	agent any
	stages {
		stage ('Build') {
			steps {
				echo 'Build'
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
