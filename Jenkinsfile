node('terraform') {
  checkout scm
  env.PATH = "/bin:/sbin:/usr/bin:/usr/sbin:/usr/local/bin:/usr/local/sbin"
  sh 'aws s3 ls'
}
