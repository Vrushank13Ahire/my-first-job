pipeline {
    agent any

    parameters {
        choice(
            name: 'ENVIRONMENT',
            choices: ['staging', 'production'],
            description: 'Target environment'
        )
    }

    stages {

        stage('Build') {
            steps {
                echo "Building"
            }
        }

        stage('Tests') {
            parallel {
                stage('Unit') {
                    steps {
                        sh 'echo Unit Test'
                    }
                }

                stage('Integration') {
                    steps {
                        sh 'echo Integration Test'
                    }
                }
            }
        }

        stage('Approve') {
            when {
                expression {
                    params.ENVIRONMENT == 'production'
                }
            }

            steps {
                input message: 'Deploy to production?'
            }
        }

        stage('Deploy') {
            steps {
                sh "echo Deploying to ${params.ENVIRONMENT}"
            }
        }
    }
}
