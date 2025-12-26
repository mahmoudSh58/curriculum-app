pipeline {
  agent any
  stages {
    stage('clone repo') {
      parallel {
        stage('clone repo') {
          steps {
            git(url: 'https://github.com/mahmoudSh58/curriculum-app.git', branch: 'master')
          }
        }

        stage('check server') {
          steps {
            sh 'date'
          }
        }

      }
    }

    stage('list repo') {
      steps {
        sh 'ls -lthr'
      }
    }

  }
}