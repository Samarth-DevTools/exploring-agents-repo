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

    stage('S3-Docker image agent') {
      agent {
        docker {
          alwaysPull true
          label 'ubuntu-docker-jdk17-node20'
          image 'node:18'
        }
      }
      steps{
        sh 'cat /etc/os-release'
        sh 'node -v'
        sh 'npm -v'
      }
    }

    stage('S4- Dockerfile agent') {
      agent {
        docker {
          image 'node:18'
          label 'ubuntu-docker-jdk17-node20'
        }
      }
      steps {
        sh ' ode -v'
        sh 'npm -v'
        sh 'cowsay -f tux this is running on docker container'
      }
    }
  }
}