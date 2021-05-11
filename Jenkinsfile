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
        stage('permissons') {
            steps {
                sh 'chmod 777 /var/jenkins_home/workspace/jenkin-devops-mircroservice1-pipeline@tmp/*/*'
            }
		}
		stage('build') {
			agent {
                docker { image 'maven:3.8.1-adoptopenjdk-11' }
            }
            steps {
                sh 'maven --version'
            }
		}
    }
}