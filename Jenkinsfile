pipeline {
  agent any
 
  stages {
    stage('Stage-1') {
      steps {
        sh 'cat /etc/os-release'
        sh 'node -v'
        sh 'npm -v'
      }
    }
    
    stage('Stage-2') {
      agent { 
          label 'ubuntu-20-docker'
      }
      steps {
        sh 'cat /etc/os-release'
        sh 'node -v'
        sh 'npm -v'
      }
    }
  }
}
