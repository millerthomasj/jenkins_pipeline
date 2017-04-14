podTemplate(
  name: 'build-myAccount',
  label: 'myaccount',
  containers: [
    containerTemplate(
      name: 'build-env',
      image: '422152100797.dkr.ecr.us-west-1.amazonaws.com/slave-terraform',
      ttyEnabled: true,
      workingDir: '/home/jenkins',
    )
  ],
  annotations: [
    podAnnotation(key: 'iam.amazonaws.com/role', value: 'jenkins_iam_role_name')
  ]
)
{
  node ('myaccount') {
    container('build-env') {
      stage('Checkout code') {
        checkout scm
      }
    }
    container('build-env') {
      stage('Run Some Command') {
        sh 'aws s3 ls'
      }
    }
  }
}
