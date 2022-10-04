pipeline {
    agent any 
     stages {
         stage('Parallel') {
          parallel {
            stage('one') {
              steps {
                echo 'sleep 30'
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
}