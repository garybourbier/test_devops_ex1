pipeline {
  agent any
  stages {
    stage('stage1') {
      steps {
        sh 'id -u ubuntu &> /dev/null'
      }
    }

    stage('stage2') {
      steps {
        sh '''find / -user ubuntu 
'''
      }
    }

    stage('stage3') {
      steps {
        sh '''find / -user ubuntu -printf "%p %s %i\\n" 
'''
      }
    }

  }
}