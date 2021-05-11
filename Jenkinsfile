//scripted pipeline, stages blocks are optional
//declarative pipeline

// node {

// 		echo "Build"
//         echo "Test"
//         echo "Integration Test"
	
// }

pipeline {
	agent {
        docker { image 'node:14-alpine' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
            }
        }
    
		stage('Build') {
			steps {
				    //sh 'docker pull maven:3.8.1'
                	echo "Build"
					sh "maven --version"
					sh "docker -- version"
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
