pipeline{
	agent any
	environment{
		DOCKER_IMAGE="dinhthong0402/yeuhan"
	}
	stages {
		stage('Checkout code') {
            steps {
                checkout scm
            }
        }
		stage('Deploy'){
			steps{
				sh "/home/ubuntu/workspace/run-yeuhan.sh"
				// sh "sudo kubectl patch deployment ${DEPLOYMENT} -p \"{\"spec\":{\"template\":{\"metadata\":{\"labels\":{\"date\":\"$(date
			}
		}
	}
	post {
		success {
		echo "SUCCESSFUL"
		}
		failure {
		echo "FAILED"
		}
	}
}