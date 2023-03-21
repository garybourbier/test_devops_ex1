pipeline {
  agent any
  stages {
    stage('Check User') {
      steps {
        script {
          def userExists = sh(returnStatus: true, script: 'id -u ubuntu >/dev/null 2>&1; echo $?').trim() == "0"
          if (userExists) {
            sh 'find / -type f -user ubuntu -printf "%s %i %p\n"'
          } else {
            error 'User "ubuntu" does not exist'
          }
        }

      }
    }

  }
}