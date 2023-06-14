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
        sh 'node server.js'
      }
    }

  }
}