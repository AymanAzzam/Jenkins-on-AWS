pipeline {
    agent any 
    stages {
        stage('Upload to AWS') {
            steps {
                withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', credentialsId: 'aws-static']]) {
                    sh 'env'
                    sh 'aws sts get-caller-identity'
                withAWS(region:'us-east-1') {
                    sh 'env'
                    sh 'aws sts get-caller-identity'
                    s3Upload(file:'index.html', bucket:'udacity-project3-jenkins', path:'index.html')
                }
                }
            }
        }
    }
}
