pipeline {
    agent any
    
    stages {
        stage ('List S3 Buckets') {
            steps {
                script {
                    withCredentials([[
                        $class: 'AmazonWebServicesCredentialsBinding',
                        credentialsId: 'aws-jenkins-integration'
                    ]]) {
                        // List all S3 buckets
                        sh 'aws s3 ls'
                    }
                }
            }
        }
    }
}
