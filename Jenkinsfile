node('build-slave') {
  stage('Build') {
      checkout scm
      sh("hostname")
      sh("aws s3 ls")
  }
}
