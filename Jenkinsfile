pipeline {
    agent {
        docker { image 'python:3.6-slim-stretch' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'python --version'
            }
        }
    }
    post {
      always {
        xUnit './out.xml'
    }
  }
}
