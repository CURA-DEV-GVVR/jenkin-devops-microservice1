//scripted pipeline, stages blocks are optional
//declarative pipeline

// node {

// 		echo "Build"
//         echo "Test"
//         echo "Integration Test"
	
// }

pipeline {
	//agent any
	agent { 
		docker {
			     image 'maven:3.8.1'
		} 
	}
	stages {
		stage('Build') {
			steps {
                	echo "Build"
					sh "maven --version"
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
