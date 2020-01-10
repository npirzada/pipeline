pipeline {
  agent any
  stages {
    stage('GCP Env Build') {
      steps {
        sh 'echo "Building GCP Environment with Terraform"'
      }
    }

    stage('Build Package') {
      steps {
        sh 'echo "Creating a Maven Build"'
      }
    }

    stage('Unit Testing') {
      steps {
        sh 'echo "Running Unit Tests"'
      }
    }

    stage('SonarQube Scan') {
      steps {
        sh 'echo "Performing Static Code Analysis"'
      }
    }

  }
}