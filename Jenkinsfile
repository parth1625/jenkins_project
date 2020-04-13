pipeline {
  agent any 
  stages {
    stage('build and test') {
      steps{
	sh '''
	. env/bin/activate
        pip3 install -r requirements.txt
	python3 manage.py test
	'''
      }
    }
    stage('Deploy to AWS') {
      steps{
	sshagent(['ssh-key']) {
	   sh '''
	   ssh -o StrictHostKeyChecking=no ubuntu@ec2-13-233-30-168.ap-south-1.compute.amazonaws.com 
	   pwd
	   whoami
	   '''
      }
	}
    }
  }
}

