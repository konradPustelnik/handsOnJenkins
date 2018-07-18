pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
        sh '''a=5
echo $a
export b=4
echo $b'''
        sh '''${a}
${b}'''
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