pipeline {
  agent { docker { image 'python:3.6' } }
  stages {
    stage('build') {
      steps{
	sh '. env/bin/activate'
        sh 'pip install --user -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        sh 'python3 manage.py test'
      }   
    }
  }
}
