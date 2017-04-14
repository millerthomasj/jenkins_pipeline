pipeline {
  agent none
  stages {
    stage('Build') {
      agent {
        label 'terraform'
      }
      steps {
        node('terraform') {
          checkout scm
          sh 'aws s3 ls'
        }
      }
    }
  }
}
