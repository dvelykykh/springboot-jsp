pipeline {
  agent {
    docker {
      image 'docker:latest'
    }
    
  }
  stages {
    stage('init') {
      steps {
        echo 'Hi there!'
        sh '''pwd
ls -a
docker -v
hostname'''
      }
    }
    stage('run') {
      steps {
        sh 'docker run --name mynginx -p 8111:80 -d nginx:alpine'
      }
    }
  }
}