pipeline {
  agent any
  stages {
    stage('Check User') {
      steps {
        script {
          def userExists = sh(script: 'id -u ubuntu 2>&1 | grep -q "no such user"; echo $?', returnStdout: true).trim().toInteger() != 0
          if (userExists) {
            error 'User "ubuntu" does not exist'
          } else {
            sh 'find / -type f -user ubuntu -printf "%s %i %p\n"'
          }
        }

      }
    }

  }
}