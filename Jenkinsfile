pipeline {
    agent any 
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(region: 'us-east-1', credentials: 'aws-static'){
                  sh '''
                  echo $AWS_ACCESS_KEY_ID
                  '''
                    
                }
            }
        }
    }
}
