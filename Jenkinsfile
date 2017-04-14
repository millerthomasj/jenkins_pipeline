podTemplate(
  name: 'build-myAccount',
  label: 'myaccount',
  containers: [
    containerTemplate(
      name: 'build-env',
      image: '422152100797.dkr.ecr.us-west-1.amazonaws.com/slave-terraform',
      ttyEnabled: true,
      workingDir: '/home/jenkins',
    ),
    containerTemplate(
      name: 'aws',
      image: 'agilestacks/aws',
      ttyEnabled: true,
      command: 'cat'
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
    container('aws') {
      stage('AWS Info') {
        sh """
          script: "aws s3 ls",
          returnStdout: true
        """
      }
    }
  }
}
