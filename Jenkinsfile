pipeline {
  agent none
  stages {
    stage('Build') {
      agent {
        label 'terraform'
      }
      steps {
        checkout scm
        sh 'echo $PATH'
        sh '''aws s3 ls'''
      }
    }
  }
}
