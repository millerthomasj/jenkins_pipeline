node('terraform') {
  stage('Build') {
    container('terraform') {
      checkout scm
      sh("hostname")
      sh("aws s3 ls")
    }
  }
}
