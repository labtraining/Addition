pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        echo 'Checkout the code'
        git(url: 'https://github.com/venkatasykam/DevOpsWebApp.git', branch: 'master', credentialsId: 'jenkigit')
      }
    }
    stage('build') {
      steps {
        echo 'build'
      }
    }
  }
}