pipeline {
    agent any 
    stages {
        stage('Upload to AWS') {
            steps {
                    s3Upload(file:'index.html', bucket:'udacity-project3-jenkins', path:'index.html')
            }
        }
    }
}
