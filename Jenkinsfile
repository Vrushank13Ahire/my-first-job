pipeline {
  agent any
  environment {
    APP_NAME = 'demo'
    BUILD_MODE = 'production' // Now globally accessible
  }
  stages {
    stage ('Build') {
      steps {
        echo "Building the application..."
      }
    }
    stage ('Test') {
      steps {
        sh 'echo $APP_NAME $BUILD_MODE'
      }
    }
  }
}
