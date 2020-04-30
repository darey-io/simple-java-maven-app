pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'ls -latr'
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'This is test stage'
            sh 'echo "This is additional Test step"'
          }
        }

        stage('Test 2') {
          steps {
            echo 'This is test 2'
          }
        }

      }
    }

    stage('Release') {
      steps {
        echo 'This is release step'
      }
    }

  }
}