@Library('jenkins-shared-library') _

pipeline {
  agent any

  parameters {
    // Defining your parameters
    string(name: 'VERSION', defaultValue: '1.0', description: 'Enter the version number')
    choice(name: 'ENVIRONMENT', choices: ['dev', 'staging', 'production'], description: 'Select the target environment')
  }

  environment {
    // Defining your environment variables
    MY_VARIABLE = 'some value'
  }

  stages {
    stage('Build') {
      steps {
        // Add build steps here
        sh 'echo "Building the project..."'
      }
    }

    stage('Test') {
      steps {
        // Add test steps here
        sh 'echo "Running tests..."'
      }
    }

    stage('Deploy') {
      steps {
        // Add deployment steps here
        sh 'echo "Deploying to ${ENVIRONMENT} environment..."'
      }
    }

    stage('Custom Stage') {
      steps {
        myCustomStep()
      }
    }
  }
}
