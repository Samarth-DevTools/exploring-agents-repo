pipeline {
  agent none
 
  stages {
    stage('Stage-1') {
      agent any
      steps {
        sh 'cat /etc/os-release'
        sh 'node -v'
        sh 'npm -v'
      }
    }
    
    stage('Stage-2') {
      agent { 
          label 'ubuntu-docker'
      }
      steps {
        sh 'cat /etc/os-release'
        sh 'node -v'
        sh 'npm -v'
      }
    }
  }
}
