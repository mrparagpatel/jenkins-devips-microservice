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
pipeline{
	agent any
	stages{
	stage('Build') {
		steps{
			echo "Build"
			echo "PATH - $PATH"
			echo "BUILD_NUMBER - $env.BUILD.NUMBER"
			echo "BUILD_ID - $env.BUILD.ID"
			echo "JOB_NAME - $env.JOB.NAME"
			echo "BUILD_TAG - $env.BUILD.TAG"
			echo "BUILD_URL - $env.BUILD.URL"
		}
	}	
	stage('Test') {
		steps{
			echo "Test"
		}
	}
	stage('NFT') {
		steps {
			echo "NFT"
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