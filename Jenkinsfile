//scripted pipeline, stages blocks are optional
//declarative pipeline

// node {

// 		echo "Build"
//         echo "Test"
//         echo "Integration Test"
	
// }

pipeline {
	agent {
        docker { dockerfile true }
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
            }
		}
    }
}