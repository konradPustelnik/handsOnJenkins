pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building'
            sh '''a=5
echo $a
b=4
echo $b
echo ${a}
echo ${b}

### echo chujek'''
            sh '''echo ${a}
echo ${b}'''
            build(job: 'KOndzik', propagate: true, wait: true, quietPeriod: 2)
          }
        }
        stage('build1') {
          steps {
            sh '''echo ${a}
echo ${b}'''
          }
        }
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
        sh '''echo ${a}
echo ${b}'''
      }
    }
  }
  environment {
    a = '5'
    b = '6'
  }
  parameters {
    choice(choices: '''yes
no''', description: 'Are you sure you want to execute this test?', name: 'run_test_only')
  }
}