pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
        sh 'npm run build'
      }
    }

    stage('Test') {
      steps {
        sh 'npm run test --no-watch --no-progress --browsers=ChromeHeadless'
      }
    }

    stage('Deploy') {
      steps {
        sh 'mv ./dist/sunrise-app /srv/sunrise-app'
      }
    }

  }
}