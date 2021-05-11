//scripted pipeline, stages blocks are optional
//declarative pipeline

// node {

// 		echo "Build"
//         echo "Test"
//         echo "Integration Test"
	
// }

pipeline {
	agent any
	// agent { 
	// 	docker {
	// 		     image 'maven:3.8.1'
	// 			 //args '-u root:root'
	// 			 //image 'node:13.8'
	// 	} 
	// }
	environment {
		mavenHome = tool "myMaven"
		dockerHome = tool "myDocker"
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"

	}
	stages {
		stage('Checkout') {
			steps {
					sh 'docker --version	'
					sh 'mvn --version'
					echo "PATH - $PATH"
					echo "BUILD_ID - $env.BUILD_ID"
					echo "JOB_NAME - $env.JOB_NAME"
					echo "BUILD_NUMBER - $env.BUILD_NUMBER"
					echo "BUILD_TAG - $env.BUILD_TAG"
					echo "BUILD_URL - $env.BUILD_URL"
			}
		}
		stage('Complie') {
			steps {
                    sh "mvn clean complie"
			}
		}
		stage('Test') {
			steps {
                    sh "mvn test"
			}
		}
		stage('Integraion Test') {
			steps {
                    sh "mvn failsafe:integration-test failsafe:verify"
			}
		}
	} 
	
	post {
		always {
			echo 'I am awesome. I run always'
		}
		success {
			echo 'I ran when you are successful'
		}
		failure {
			echo 'I run when you fail'
		}
		//changed,  unstable
	}


}
