pipeline {
  agent none
  stages {
    stage('Build') {
      agent {
        label 'terraform'
      }
      steps {
        checkout scm
      }
    }
  }
}
