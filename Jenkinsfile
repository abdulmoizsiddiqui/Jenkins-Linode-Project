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
        sh '''docker build Jenkins-Linode-Project/Dockerfile .
'''
      }
    }

    stage('Login to DockerHub') {
      environment {
        DOCKERHUB_USER = '$DOCKERHUB_USER'
        DOCKERHUB_PASSWORD = '$DOCKERHUB_PASSWORD'
      }
      steps {
        sh 'docker login -u $DOCKERHUB_USER -p $DOCKERHUB_PASSWORD'
      }
    }

  }
}
