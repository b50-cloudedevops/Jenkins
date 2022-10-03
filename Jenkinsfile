pipeline {
       agent  any

       environment {
        SSH_CRED= credentials('SSH')
        ENV_URL="pipeline.google.com"
       }
       triggers { pollSCM('*/2 * * * *') }
       tools {
        maven 'maven-3.8.5'
       }
       parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
       }

               stages {
                   stage('This is first stage') {
                       steps {
                          sh "echo ${ENV_URL}" 
                        }
                        input { 
                         message "Should we continue?"
                           ok "Yes, we should."
                          submitter "alice,bob"
                    }
                    stage("This is second stage") {
                     environment {
                        ENV_URL="stgaed.google.com"
                                  } 
                        steps {
                            sh  "echo environment URL is  ${ENV_URL}"
                            echo "hello Vamsi"
                        }
                    }
                }
            
}
