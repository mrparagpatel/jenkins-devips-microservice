//SCRIPTIVE
// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// 		stage('NFT Test') {
// 		echo "NFTTest"
// 	}
// }

//DECLARATIVE
pipeline {
	agent any
	environment {
//		dockerHome = tool 'myDocker'
		mavenHome = tool 'MyMaven'
//		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
		PATH = "$mavenHome/bin:$PATH"
	}

	stages {
	stage('Build') {
		steps {
			sh 'mvn --version'
			sh 'docker --version'
			echo "Build"
			echo "PATH - $PATH"
			echo "BUILD_NUMBER - $env.BUILD_NUMBER"
			echo "BUILD_ID - $env.BUILD_ID"
			echo "JOB_NAME - $env.JOB_NAME"
			echo "BUILD_TAG - $env.BUILD_TAG"
			echo "BUILD_URL - $env.BUILD_URL"
		}
	}	
	stage('Test') {
		steps {
			echo "Test"
		}
	}
	stage('NFT') {
		steps {
			echo "NFT"
		}
	}
	}
	post {
		always {
			echo 'I always run'
		}
		success {
			echo 'I run when all stages are successful'
		}
		failure {
			echo 'I run when a stage fails'
		}
	}
}
