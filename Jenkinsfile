pipeline {
    agent any 

    parameters {
        string(name: 'VERSION', defaultValue: '1.0', description: 'Version to deploy')
        choice(name: 'ENVIRONMENT', choices: ['staging', 'production'], description: 'Target environment')
        booleanParam(name: 'SKIP_TESTS', defaultValue: false, description: 'Skip testing phase?')
    }

    stages {
        stage('Build') {
            steps {
                echo "Building"
            }
        }

        
    }
}
