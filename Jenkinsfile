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
        sh 'ng test --no-watch --no-progress --source-map=false --browsers=PhantomJS'
      }
    }

    stage('Deploy') {
      steps {
        sh 'sh ../../scripts/deploy.sh'
      }
    }

  }
}