pipeline {
  agent any
  stages {
    stage('stage1') {
      steps {
        sh '''sudo apt-get -y update && sudo apt-get -y upgrade
'''
      }
    }

    stage('stage2') {
      steps {
        sh 'dpkg -l > /tmp/pkg'
      }
    }

    stage('stage3') {
      steps {
        sh 'if [ \'grep -c git /tmp/pkg\' -ne 0]'
      }
    }

  }
}