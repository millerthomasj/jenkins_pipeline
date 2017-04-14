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
        sh 'which aws'
        sh 'which echo'
        sh '''aws s3 ls'''
      }
    }
  }
}
