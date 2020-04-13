pipeline {
  agent any 
  stages {
    stage('build') {
      steps{
	sh '''
	. env/bin/activate
        pip3 install -r requirements.txt
	python3 manage.py test
	'''
      }
    }
  }
}
