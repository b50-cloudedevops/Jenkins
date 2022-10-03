pipeline {
       agent  any

       environment {
         ENV_URL="pipeline.google.com"
       }
               stages {
                   stage('This is first stage') {
                       steps {
                          sh "echo ${ENV_URL}" 
                        }
                    }
                    stage("This is second stage") {
                        steps {
                            sh  "echo environment URL is  ${ENV_URL}"
                        }
                    }
                }
            
}
