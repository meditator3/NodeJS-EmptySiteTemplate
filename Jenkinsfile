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
        sh 'node server.js &'
      }
    }

    stage('Test') {
      steps {
        sh '''curl 192.168.14.33:8080
'''
      }
    }

    stage('Artifact') {
      steps {
        sh '''


  
ls -alh'''
        sh '''tar -czvf nodejs.tar.gz   
\\*'''
        archiveArtifacts '*.tar.gz'
      }
    }

  }
}