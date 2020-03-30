pipeline {
    agent any 
    environment {
        AWS_ID = credentials("ASIA22DCAELIDP2QUHU7")
        AWS_ACCESS_KEY_ID = AWS_ID
        AWS_SESSION_TOKEN = "${env.AWS_ID_USR}"
        AWS_SECRET_ACCESS_KEY = "${env.AWS_ID_PSW}"
    }
    stages {
        stage('Upload to AWS') {
            steps {
        
                  s3Upload(file:'index.html',bucket: 'udacity-project3-jenkins', path: "index.html")
                
            }
        }
    }
}
