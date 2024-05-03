pipeline {
  agent none
  stages {
    stage('Back-end') {
      agent {
        docker { image 'nginx' }
      }
      steps {
        sh 'nginx --verion'
      }
    }
    stage('Front-end') {
      agent {
        docker { image 'node:16-alpine' }
      }
      steps {
        sh 'echo "hello world version $(node --version) of node"
      }
    }
  }
}
