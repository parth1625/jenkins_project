pipeline {
  agent { docker { image 'python:3.7.2' } }
  stages {
    stage('build') {
      steps {
	sh 'apt install virtualenv -y'
	sh 'virtualenv env'
	sh 'source env/bin/activate'
        sh 'pip install -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        sh 'python3 manage.py test'
      }   
    }
  }
}
