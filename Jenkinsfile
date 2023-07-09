pipeline {
  agent any
  stages {
    stage('Code Review') {
      steps {
        git(url: 'https://github.com/abdulmoizsiddiqui/feedback-app.git', branch: 'master')
      }
    }

    stage('log') {
      steps {
        sh 'ls -la'
      }
    }

  }
}