pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh '/usr/local/bin/aws sts get-caller-identity'
                sh '/usr/local/bin/aws cloudformation create-stack --stack-name my-first-ec2-stack --template-body file://./EC2/ec2.yaml'
            }
        }
    }
}