pipeline {
// Testing
  agent none
  stages {
    stage('Build') {
      node('terraform') {
        steps {
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
