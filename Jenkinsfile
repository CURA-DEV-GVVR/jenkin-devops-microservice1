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
		stage('build') {
			agent {
                docker { image 'maven:3.8.1-adoptopenjdk-11' }
            }
            steps {
                bash 'maven --version'
            }
		}
    }
}