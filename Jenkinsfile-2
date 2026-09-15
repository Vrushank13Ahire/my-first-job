pipeline {
    agent any

    stages {
        stage('Test') {
            parallel {
                stage('Unit') {
                    steps {
                        sh 'echo Running Tests'
                    }
                }

                stage('Integration') {
                    steps {
                        sh 'echo Running integration test'
                    }
                }
            }
        }
    }
}
