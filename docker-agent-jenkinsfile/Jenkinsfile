pipeline {
  agent none
  stages {
    stage('Back-end') {
      agent {
        docker { image 'nginx' }
      }
      steps {
        sh 'nginx -v'
      }
    }
    stage('Front-end') {
      agent {
        docker { image 'node:16-alpine' }
      }
      steps {
        sh 'echo "hello node version: $(node --version)"'
      }
    }
  }
}
