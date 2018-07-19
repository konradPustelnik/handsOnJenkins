pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''
a = 5
'''
      }
    }
    stage('Test') {
      parallel {
        stage('Test Chrome') {
          steps {
            sh 'echo \'Test Chrome\''
          }
        }
        stage('Test Edge') {
          steps {
            echo 'Done'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'sadsa'
      }
    }
  }
}