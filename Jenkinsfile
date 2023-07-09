pipeline {
  agent any
  stages {
    stage('Code Review') {
      steps {
        git(url: 'https://github.com/abdulmoizsiddiqui/feedback-app.git', branch: 'master')
      }
    }

    stage('docker') {
      steps {
        sh 'ls -la'
      }
    }

  }
}