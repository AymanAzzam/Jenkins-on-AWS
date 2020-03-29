pipeline {
    agent any 
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(region: 'us-east-1', credentials: 'aws-static'){
                  sh '''
                  export AWS_SESSION_TOKEN="FwoGZXIvYXdzEPP//////////wEaDJJ9Ty3Aq3EUSCGN6yLFAab8BN8jodvZaHxnOo/VGcnviI+HdTKYe3JrOdVV/KwMMZVDnBCtyzkXUllYdwmXcooypkVInLIVFuOt7bZZ3ROhVOT2bp1Y6Ti1t/dzJioaajTNV1jpeCEfJTTNoxJcYr8eV4tCzUY/5YVPMZmQqpFADPShCaqPZFNNQfwebOWO5t+1k5N6VSEfdgVYe33i2WI/b20L1+3aXbtctYTonH7FSQHPeIxxWpJISyEox3s2Ea2EHZ2TGuYUu/tnEEODkMAfc4/LKP22g/QFMi3fEGL/KIirjiBZ7QwS45CLg7HIpjfBuzwuPbIqCNRXHPMsIBpK1FFuiNxh7kU="
                  echo $AWS_ACCESS_KEY_ID
                  echo $AWS_SECRET_ACCESS_KEY
                  echo $AWS_SESSION_TOKEN
                  '''
                  s3Upload(file:'index.html',bucket: 'udacity-project3-jenkins', path: "index.html")
                }
            }
        }
    }
}
