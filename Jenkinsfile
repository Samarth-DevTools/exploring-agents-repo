pipeline {
  agent {
    dockerfile {
      filename 'Dockerfile.cowsay'
      label 'ubuntu-docker-jdk17-node20'
    }
  }
 
  stages {
    stage('S1-Any Agent') {
      steps {
        sh 'cat /etc/os-release'
        sh 'node -v'
        sh 'npm -v'
      }
    }
    
    stage('S2-Ubuntu Agent') {
      steps {
        sh 'cat /etc/os-release'
        sh 'node -v'
        sh 'npm -v'
      }
    }

    stage('S3-Docker image agent') {
      steps{
        sh 'cat /etc/os-release'
        sh 'node -v'
        sh 'npm -v'
      }
    }

    stage('S4- Dockerfile agent') {
      steps {
        sh 'node -v'
        sh 'npm -v'
        sh 'cowsay -f tux this is running on docker container'
      }
    }
  }
}