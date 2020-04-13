pipeline {
  agent { docker { image 'python:3.7.2' } }
  stages {
    stage('build') {
      steps {
        sh 'sudo pip install -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        sh 'sudo python3 manage.py test'
      }   
    }
  }
}
