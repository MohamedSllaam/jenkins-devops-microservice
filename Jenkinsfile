// node {
// 		echo "Build"
// 		echo "Test"	
// 		echo "Integration Test"
// }
pipeline {
 agent any
	// agent {
	// 	docker {
	// 		image 'maven:3.8.4-openjdk-17'
	// 	 args '-v /root/.m2:/root/.m2'
	// 	}
	// }
	// agent {
	// 	docker {
	// 		image 'node:18-alpine'
	// 		args '-v /root/.npm:/root/.npm'
	// 		}
	// }
	environment {
		dockerHome='MyDocker'
		mavenHome='MyMaven'
		PATH="$dockerHome/bin:$mavenHome/bin:$PATH"
	 
	}
	stages {
		stage('Build') {
			steps {
				 sh 'mvn --version'
				 sh 'docker version'
				echo "Build"
				echo "$PATH"
				echo "BUILD_NUMBER: ${env.BUILD_NUMBER}"
				echo "BUILD_ID: ${env.BUILD_ID}"
				echo "BUILD_TAG: ${env.BUILD_TAG}"
				echo "BUILD_URL: ${env.BUILD_URL}"
				echo "WORKSPACE: ${env.WORKSPACE}"
				echo "JOB_NAME: ${env.JOB_NAME}"
				echo "GIT_COMMIT: ${env.GIT_COMMIT}"	
				echo "GIT_BRANCH: ${env.GIT_BRANCH}"
				echo "GIT_URL: ${env.GIT_URL}"
				
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
