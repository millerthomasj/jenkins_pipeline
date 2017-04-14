pipeline {
// Testing
  agent none
  stages {
    node('terraform') {
      stage('Build') {
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
