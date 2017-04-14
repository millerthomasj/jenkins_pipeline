pipeline {
  agent none
  stages {
    stage('Build') {
      steps {
        node('terraform') {
          checkout scm
          env.PATH = "/usr/bin:/usr/sbin:/usr/local/bin:/usr/local/sbin"
          sh 'aws s3 ls'
        }
      }
    }
  }
}
