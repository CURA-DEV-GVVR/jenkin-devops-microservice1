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
	stages {
		stage('Build') {
			steps {
				    //sh 'docker pull maven:3.8.1'
                	echo "Build"
					//sh "maven --version"
					echo "$PATH"
					echo "BUILD_ID - $env.BUILD_ID"
					echo "JOB_NAME - $env.JOB_NAME"
					echo "BUILD_NUMBER - $env.BUILD_NUMBER"
					echo "BUILD_TAG - $env.BUILD_TAG"
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
