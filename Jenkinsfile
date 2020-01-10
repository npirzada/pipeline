pipeline {
  agent any
  stages {
    stage('GCP Env Build') {
      steps {
        sh '''sleep 10
echo "Building GCP Environment with Terraform"'''
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

    stage('Nexus IQ Scan') {
      steps {
        sh 'echo "Nexus IQ Scan"'
      }
    }

    stage('Nexus  Deployment') {
      steps {
        sh 'echo "package deployed to repository"'
      }
    }

    stage('InSpec Scan') {
      steps {
        sh 'Echo "Environmet Chef Scan "'
      }
    }

    stage('Deploy to Dev') {
      steps {
        sh 'echo "Deploy to Dev"'
      }
    }

    stage('InSpec Scan Dev') {
      steps {
        sh 'echo "Deploy to Dev"'
      }
    }

    stage('Deploy to QA') {
      steps {
        sh 'echo "Deploy to QA"'
      }
    }

    stage('InSpec Scan QA') {
      steps {
        sh 'echo "InSpec Scan"'
      }
    }

    stage('QA Automated Testing') {
      parallel {
        stage('QA Automated Testing') {
          steps {
            sh 'echo "Selinum testing"'
          }
        }

        stage('Smoke Test') {
          steps {
            sh 'echo "smoke"'
          }
        }

        stage('Regression Tests') {
          steps {
            sh 'echo "regression testing"'
          }
        }

      }
    }

    stage('Vericode Scan') {
      steps {
        sh 'echo "Vericode Scan"'
      }
    }

    stage('InSpec Scan Prod') {
      steps {
        sh 'echo "test"'
      }
    }

    stage('Deploy to Prod') {
      steps {
        sh 'echo "test"'
      }
    }

  }
}