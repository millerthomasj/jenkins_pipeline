pipeline {
  agent none
  stages {
    stage('Build') {
      agent {
        label 'terraform'
      }
      steps {
        checkout scm
        sh '/usr/local/bin/aws s3 ls'
      }
    }
  }
}
