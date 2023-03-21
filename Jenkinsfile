pipeline {
  agent any
  stages {
    stage('Check if user exists') {
      steps {
        script {
          sh 'id -u user &> /dev/null'
          if (returnStatus == 0) {
            echo 'User exists'
          } else {
            error 'User does not exist'
          }
        }

      }
    }

    stage('Find files owned by user') {
      steps {
        script {
          sh 'find / -user user -print 2>/dev/null > files.txt'
          sh 'cat files.txt'
        }

      }
    }

    stage('Display file sizes and inodes') {
      steps {
        script {
          sh 'find / -user user -printf "%p %s %i\n" 2>/dev/null > file_info.txt'
          sh 'cat file_info.txt'
        }

      }
    }

  }
}