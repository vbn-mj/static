pipeline{
        agent any
        stages {
              stage('Upload to AWS') {
                steps {
                    retry(3){
                        withAWS(region:'us-west-2', credentials:'aws-static'){
                        s3Upload(file:'index.html', bucket:'jenkins-cloud-devops', path:'index.html')
                    }                             
                }
            }
        }
    }
    }
