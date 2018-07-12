pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
      }
    }
    stage('Test Chrome') {
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