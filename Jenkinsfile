pipeline {
    agent any 
    stages {
        stage('Upload to AWS') {
            steps {
                withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', credentialsId: 'aws-static']]) {
                    sh 'env'
                    sh 'aws sts get-caller-identity'
                }
            }
        }
    }
}
