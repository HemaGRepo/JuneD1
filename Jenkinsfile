pipeline {
  agent any
  stages {
    stage('Fetch Code') {
      parallel {
        stage('Step1') {
          steps {
            echo 'Fetching code'
          }
        }
        stage('') {
          steps {
            echo 'Clone the git repo'
          }
        }
      }
    }
    stage('Build the code') {
      parallel {
        stage('Step 2') {
          steps {
            echo 'Build The code'
          }
        }
        stage('') {
          steps {
            bat 'javac HelloWorld.java'
          }
        }
      }
    }
    stage('Deploy the code') {
      parallel {
        stage('Step 3') {
          steps {
            echo 'Deploy'
          }
        }
        stage('') {
          steps {
            bat 'java HelloWorld'
          }
        }
      }
    }
    stage('Step 4') {
      steps {
        echo 'Create Reports'
      }
    }
  }
}