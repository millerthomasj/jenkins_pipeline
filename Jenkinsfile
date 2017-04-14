pipeline {
// Testing
  agent none

  stages {
    stage('Build') {
      steps {
        node('slave-terraform') {
          container('terraform') {
            checkout scm
            sh("hostname")
            sh("aws s3 ls")
          }
        }
      }
    }
  }
}
