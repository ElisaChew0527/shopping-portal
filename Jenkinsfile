pipeline {
  agent any
  stages {
    stage('build-the-app') {
      steps {
        echo 'build job'
        sh 'npm install'
      }
    }

    stage('test-the-app') {
      steps {
        echo 'test job'
        sh 'npm test'
      }
    }

    stage('package-the-job') {
      steps {
        echo 'package job'
        sh 'npm run package'
      }
    }

    stage('Archive') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'this pipeline for shopping-portal has completed...'
    }

  }
}