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
        sh '''git clone https://github.com/apache/httpd.git

'''
      }
    }

    stage('Unit Testing') {
      steps {
        sh '''sleep 5
echo "Running Unit Tests"'''
      }
    }

    stage('SonarQube Scan') {
      parallel {
        stage('SonarQube Scan') {
          steps {
            sh '''sleep 10
echo "Performing Static Code Analysis"'''
          }
        }

        stage('TwistLock Scan') {
          steps {
            sh 'echo "Twistlock Container Scan"'
          }
        }

      }
    }

    stage('Nexus IQ Scan') {
      steps {
        sh '''sleep 6
echo "Nexus IQ Scan"'''
      }
    }

    stage('Nexus  Deployment') {
      steps {
        sh '''sleep 7
echo "package deployed to repository"'''
      }
    }

    stage('InSpec Scan Dev') {
      steps {
        sh '''sleep 7
echo "Environmet Chef Scan "'''
      }
    }

    stage('Deploy to Dev') {
      steps {
        sh '''sleep 5
echo "Deploy to Dev"'''
      }
    }

    stage('InSpec Scan QA') {
      steps {
        sh '''sleep 5
echo "Deploy to Dev"'''
      }
    }

    stage('Deploy to QA') {
      steps {
        sh '''sleep 5
echo "Deploy to QA"'''
      }
    }

    stage('QA Automated Testing') {
      parallel {
        stage('QA Automated Testing') {
          steps {
            sh '''sleep 5
echo "Selinum testing"'''
          }
        }

        stage('Smoke Test') {
          steps {
            sh '''sleep 5
echo "smoke"'''
          }
        }

        stage('Regression Tests') {
          steps {
            sh '''sleep 5
echo "regression testing"'''
          }
        }

      }
    }

    stage('Vericode Scan') {
      steps {
        sh '''sleep 5
echo "Vericode Scan"'''
      }
    }

    stage('InSpec Scan Prod') {
      steps {
        sh '''sleep 5
echo "test"'''
      }
    }

    stage('Deploy to Prod') {
      steps {
        sh '''sleep 5
echo "test"'''
      }
    }

    stage('Prod Automated Vlidation') {
      steps {
        sh 'echo "Deploy package to production"'
      }
    }

    stage('Vericode Scan ?') {
      steps {
        sh 'echo "Production Vericode Scan"'
      }
    }

  }
}