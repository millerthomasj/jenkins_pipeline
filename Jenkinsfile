pipeline {
  agent none
  stages {
    stage('Build') {
      node('terraform') {
        agent {
          label 'terraform'
        }
        steps {
          checkout scm
          sh 'aws s3 ls'
        }
      }
    }
  }
}
