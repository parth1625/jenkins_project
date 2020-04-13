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
	sh '''
	ssh -o StrictHostKeyChecking=no ubuntu@ec2-13-232-218-1.ap-south-1.compute.amazonaws.com
	pwd
	whoami
	'''
      }
    }
  }
}

