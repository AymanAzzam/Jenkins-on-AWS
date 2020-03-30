pipeline {
    agent any 
    environment {
        AWS_ID = credentials("ASIA22DCAELIFETMUJPO")
        AWS_ACCESS_KEY_ID = "ASIA22DCAELIFETMUJPO"
        AWS_SESSION_TOKEN = "${env.AWS_ID_USR}"
        AWS_SECRET_ACCESS_KEY = "${env.AWS_ID_PSW}"
    }
    stages {
        stage('Lint HTML') {
            steps {
                sh tidy -q -e *.html
            }
        }
        stage('Upload to AWS') {
            steps {
                  s3Upload(file:'index.html',bucket: 'udacity-project3-jenkins', path: "index.html")
            }
        }
    }
}
