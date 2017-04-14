pipeline {
  agent none
  stages {
    stage('Build') {
      steps {
        node('terraform') {
          checkout scm
          sh 'aws s3 ls'
        }
      }
    }
  }
}
