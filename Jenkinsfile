pipeline {
  agent {
    node {
      label 'docker'
    }

  }
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/meditator3/NodeJS-EmptySiteTemplate.git', branch: 'master')
      }
    }

    stage('Build') {
      steps {
        sleep 2
        sh 'node server.js'
      }
    }

  }
}