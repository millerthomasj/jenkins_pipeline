pipeline {
// Testing
  agent none
      node('terraform') {
  stages {
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
