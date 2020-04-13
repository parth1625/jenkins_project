pipeline {
  agent { docker { image 'python:3.6' } }
  stages {
    stage('build') {
      steps{
	sh '. env/bin/activate'
        sh 'pip3 install -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        sh 'python3 manage.py test'
      }   
    }
  }
}
