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
        sh '''sudo find / -user ubuntu -print
'''
      }
    }

    stage('stage3') {
      steps {
        sh '''sudo find / -user ubuntu -printf "%p %s %i\\n" 
'''
      }
    }

  }
}