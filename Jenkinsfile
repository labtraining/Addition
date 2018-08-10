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
    stage('sonar') {
      steps {
        echo 'sonar analysis'
      }
    }
    stage('deploy-package-nexus') {
      parallel {
        stage('deploy-nexus') {
          steps {
            echo 'deploy-package-nexus'
          }
        }
        stage('deploy-server') {
          steps {
            echo 'deploy the package to application server/environemnt'
          }
        }
      }
    }
    stage('test') {
      steps {
        echo 'selenium testting'
      }
    }
    stage('deploy-system') {
      steps {
        echo 'deploy-to-higher env system'
      }
    }
    stage('test-on-system') {
      steps {
        echo 'testing on system env'
      }
    }
  }
}