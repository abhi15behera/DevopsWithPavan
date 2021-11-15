pipeline {
  agent any
  stages {
    stage('Connect to GIT') {
      parallel {
        stage('ConnecttoGIT') {
          steps {
            git(url: 'https://github.com/abhi15behera/DevopsWithPavan.git', branch: 'master')
          }
        }

        stage('printmessage') {
          steps {
            echo 'Welcome to GitHub'
          }
        }

      }
    }

    stage('Run Py Code') {
      parallel {
        stage('Run Py Code') {
          steps {
            sh 'python hello.py '
          }
        }

        stage('print message') {
          steps {
            echo 'Running the code successfully'
          }
        }

      }
    }

  }
}