pipeline {
    agent {
        label 'Slave'
    }
     stages {
         stage('Parallel') {
          parallel {
            stage('one') {
              steps {
                echo 'sleep 30'
                sh "hostname"
                }
          }

          stage('two') {
            steps {
                echo 'sleep 30'
            }
         }
       }
    }

  }
     post {
        success {
            cleanWs()
        }
     
     }
}