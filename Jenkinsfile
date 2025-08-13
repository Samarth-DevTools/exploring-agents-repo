pipeline {
  agent {
    dockerfile {
      filename 'Dockerfile.cowsay'
      label 'ubuntu-docker-jdk17-node20'
    }
  }
 
  stages {
    stage('Stage-1') {
      steps {
        sh 'cat /etc/os-release'
        sh 'node -v'
        sh 'npm -v'
        echo "#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*"
        sh 'echo $((RANDOM)) > /tmp/imp-file-$BUILD_ID'
        sh 'ls -ltr/tmp/imp-file-$BUILD_ID'
        sh cat /tmp/imp-file-$BUILD_ID'
        echo "#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#"
      }
    }

    stage('S2-Ubuntu Agent') {
      steps {
        sh 'cat /etc/os-release'
        sh 'node -v'
        sh 'npm -v'
        echo "#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*"
        sh 'ls -ltr/tmp/imp-file-$BUILD_ID'
        sh 'cat /tmp/imp-file-$BUILD_ID'
        echo "#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#"
      }
    }

    stage('S3-Docker image agent') {
      steps{
        sh 'cat /etc/os-release'
        sh 'node -v'
        sh 'npm -v'
        echo "#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*"
        sh 'ls -ltr/tmp/imp-file-$BUILD_ID'
        sh 'cat /tmp/imp-file-$BUILD_ID'
        echo "#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#"
      }
    }

    stage('S4- Dockerfile agent') {
      steps {
        sh 'node -v'
        sh 'npm -v'
        sh 'cowsay -f tux this is running on docker container'
        echo "#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*"
        sh 'ls -ltr/tmp/imp-file-$BUILD_ID'
        sh 'cat /tmp/imp-file-$BUILD_ID'
        echo "#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#"
        sh 'sleep 120s'
      }
    }
  }
}