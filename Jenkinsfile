pipeline {
// Testing
  agent none

  stages {
    stage('Build') {
      steps {
        node('terraform') {
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
