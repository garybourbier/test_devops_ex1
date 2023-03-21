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
        sh '''find / -user ubuntu -print 2>/dev/null
'''
      }
    }

    stage('stage3') {
      steps {
        sh '''find / -user ubuntu -printf "%p %s %i\\n" 2>/dev/null
'''
      }
    }

  }
}