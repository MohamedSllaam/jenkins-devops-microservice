// node {
// 		echo "Build"
// 		echo "Test"	
// 		echo "Integration Test"
// }
pipeline {
	// agent any
	// agent {
	// 	docker {
	// 		image 'maven:3.8.4-openjdk-17'
	// 	 args '-v /root/.m2:/root/.m2'
	// 	}
	// }
	agent {
		docker {
			image 'node:18-alpine'
			args '-v /root/.npm:/root/.npm'
			}
	}
	stages {
		stage('Build') {
			steps {
				sh 'node --version'
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
												echo 'This will always run'
								}
								success {
												echo 'This will run only if successful'
								}
								failure {
												echo 'This will run only if failed'
								}
				}
}
// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// 	stage('Integration Test') {
// 		echo "Integration Test"
// 	}
// }
