pipeline {
  agent any
  stages {
    stage('init') {
      steps {
        sh 'echo "hello"'
        sh 'echo "hello again"'
      }
    }
    stage('Build') {
      steps {
        parallel(
          "Build": {
            sh 'echo "build for centos"'
            
          },
          "Build for ubuntu": {
            sh 'echo "ubuntu"'
            
          }
        )
      }
    }
    stage('deploy') {
      steps {
        sh 'echo "deploy"'
      }
    }
  }
}