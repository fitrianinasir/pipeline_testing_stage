pipeline {
  agent any
  stages{
    stage('PROD Env'){
      steps{
        sh 'echo running PROD env 2'
      }
    }
    stage('Submit Stack'){
      steps{
        sh 'cat 01_s3cft.yml'
        sh "aws cloudformation create-stack --stack-name s3bucket --template-body file://01_s3cft.yml --region 'us-west-2'"
      }
    }
  }
}