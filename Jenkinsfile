pipeline {
  agent any
  stages {
    stage('Build') {
      environment {
        a = '5'
        b = '6'
      }
      steps {
        echo 'Building'
        sh '''a=5
echo $a
b=4
echo $b
echo ${a}
echo ${b}'''
        sh '''echo ${a}
echo ${b}'''
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