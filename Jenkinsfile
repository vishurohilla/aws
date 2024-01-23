pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''pwd
date'''
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'This is test stage'
          }
        }

        stage('test par') {
          steps {
            echo 'side by side'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'This is deploy state'
        sleep 20
      }
    }

  }
}