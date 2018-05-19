pipeline {
  agent none
  stages {
    stage('checkout') {
      steps {
        echo 'checkout'
      }
    }
    stage('build') {
      parallel {
        stage('module1') {
          steps {
            echo 'module1'
          }
        }
        stage('module2') {
          steps {
            echo 'module2'
          }
        }
      }
    }
    stage('test') {
      parallel {
        stage('static analysis') {
          steps {
            echo 'static analysis'
          }
        }
        stage('functional tests') {
          steps {
            echo 'functional tests'
          }
        }
        stage('sonarQube publication') {
          steps {
            echo 'sonarqube publication'
          }
        }
      }
    }
    stage('deploy') {
      steps {
        echo 'deploy'
      }
    }
  }
}