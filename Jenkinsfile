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
        sh '#!/bin/bash; /usr/local/bin/aws s3 ls'
      }
    }
  }
}
