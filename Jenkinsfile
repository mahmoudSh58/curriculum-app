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

    stage('intall npm') {
      steps {
        sh '''#!/bin/bash

# Check if npm is installed
if ! command -v npm &> /dev/null
then
    echo "npm could not be found. Installing now..."
    
    # Update package lists
    apt update
    
    # Install Node.js and npm
    # On many distros, \'npm\' is a separate package from \'nodejs\'
    apt install -y nodejs npm
    
    echo "Installation complete."
else
    echo "npm is already installed (Version: $(npm -v))"
fi'''
      }
    }

    stage('front end') {
      steps {
        sh 'docker --version'
      }
    }

  }
}