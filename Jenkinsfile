podTemplate(
  name: 'build-myAccount',
  label: 'myaccount',
  containers: [
    containerTemplate(
      name: 'awscli',
      image: 'fstab/aws-cli',
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
    stage('Get myAccount code') {
      container('awscli') {
        stage('Test AWS CLI') {
          sh 'aws s3 ls'
        }
      }
    }
  }
}
