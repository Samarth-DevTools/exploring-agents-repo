pipeline {
  agent any
 
  stages {
    stage('S1-Any Agent') {
      steps {
        sh 'cat /etc/os-release'
        sh 'node -v'
        sh 'npm -v'
      }
    }
    
    stage('S2-Ubuntu Agent') {
      agent { 
          label 'ubuntu-docker-jdk17-node20'
      }
      steps {
        sh 'cat /etc/os-release'
        sh 'node -v'
        sh 'npm -v'
      }
    }
  }
}
