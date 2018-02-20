pipeline {
   agent any
   stages {
     stage('Build and Test') {
        steps {
            sh 'echo Hello'
        }
     }
   }
   post {
      always {
        junit '**/*.xml'
      }
   } 
}
