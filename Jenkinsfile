pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        echo 'Building the application'
        sh 'g++ main.cpp -o main.out'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing the application'
        sh 'chmod +x main.out'
        sh './main.out'
      }
    }
  }

  post {
    success {
      archiveArtifacts artifacts: 'main.out', fingerprint: true
    }
  }
}
