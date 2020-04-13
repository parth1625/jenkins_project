pipeline {
  agent { docker { image 'python:3.7.2' } }
  stages {
    stage('build') {
      steps{
	sh '. env/bin/activate'
        sh 'pip install -r requirements.txt --user'
      }
    }
    stage('test') {
      steps {
        sh 'python3 manage.py test'
      }   
    }
  }
}
