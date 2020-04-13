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
	withAWS(credentials: '3dc5e9f8-a132-497e-9fd7-933ed050ff11', region: 'ap-south-1') {
	pwd
	whoami
	'''
      }
    }
  }
}
