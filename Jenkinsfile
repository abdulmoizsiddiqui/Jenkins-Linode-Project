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

    stage('Build') {
      steps {
        sh '''docker build -f Jenkins-Linode-Project .
'''
      }
    }

    stage('Login to DockerHub') {
      environment {
        DOCKERHUB_USER = 'abdulmoizsiddiqui'
        DOCKERHUB_PASSWORD = 'Abdulmoiz123'
      }
      steps {
        sh 'docker login -u $DOCKERHUB_USER -p $DOCKERHUB_PASSWORD'
      }
    }

  }
}