pipeline {
       agent  any

       environment {
        SSH_CRED= credentials('SSH')
        ENV_URL="pipeline.google.com"
       }
       triggers { pollSCM('*/2 * * * *') }
       parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

               stages {
                   stage('This is first stage') {
                       steps {
                          sh "echo ${ENV_URL}" 
                        }
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
