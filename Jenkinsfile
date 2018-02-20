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
        junit 'out.xml'
        // step([$class: 'XUnitBuilder',
                // thresholds: [[$class: 'FailedThreshold', unstableThreshold: '1']],
                // tools: [[$class: 'JUnitType', pattern: '**/out.xml']]])
    }
  }
}
