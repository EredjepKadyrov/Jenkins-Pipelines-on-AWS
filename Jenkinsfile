pipeline{
        agent any
        stages {
            stage('Upload to AWS') {
                steps {
                    retry(3){
                        withAWS(region:'us-west-2', credentials:'aws-static'){
                        s3Upload(file:'index.html', bucket:'vivek.tech.jenkins', path:'')
                    }                             
                }
            }
        }
    }
}
