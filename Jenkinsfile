pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'cd /home/tanya/;sh build.sh'
      }
    }
    stage('User testing') {
      parallel {
        stage('chrome') {
          steps {
            echo 'chrome'
          }
        }
        stage('firfox') {
          steps {
            echo 'firefox'
          }
        }
        stage('safari') {
          steps {
            echo 'safari'
          }
        }
      }
    }
    stage('Analysis') {
      steps {
        sleep 10
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy Testing Env'
      }
    }
  }
}