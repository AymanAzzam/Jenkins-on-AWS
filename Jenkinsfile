pipeline {
    agent any 
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(region: 'us-east-1', credentials: 'aws-static'){
                    sh 'env'
                    sh 'aws sts get-caller-identity'
                    s3Upload(file:'index.html', bucket:'udacity-project3-jenkins', path:'index.html')
                }
            }
        }
    }
}
