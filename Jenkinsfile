//scripted pipeline, stages blocks are optional
//declarative pipeline

// node {

// 		echo "Build"
//         echo "Test"
//         echo "Integration Test"
	
// }

pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
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
			echo 'I am awesome. I run always'
		}
		success {
			echo 'I ran when you are successful'
		}
		failure {
			echo 'I run when you fail'
		}
	}


}
