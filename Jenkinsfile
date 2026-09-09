pipeline {
  agent any
  environment {
    APP_NAME = 'demo'
  }
  stages {
    stage ('Build') {
      steps {
        echo "Building..."
      }
    }
    stage ('Test') {
      environment {
        BUILD_MODE = 'production' // Locally accessible only in this stage
      }
      steps {
        sh 'echo $APP_NAME $BUILD_MODE'
      }
    }
  }
}
