pipeline {
  agent any
  stages {
    stage('clone repo') {
      steps {
        git(url: 'https://github.com/mahmoudSh58/curriculum-app.git', branch: 'master')
      }
    }

    stage('list repo') {
      steps {
        sh 'ls -lthr'
      }
    }

    stage('front end') {
      steps {
        sh '''cd curriculum-front
npm i
npm run test:unit'''
      }
    }

  }
}