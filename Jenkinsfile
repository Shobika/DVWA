pipeline {
  stage('Checkout Code from GitHub Repository') {
    checkout scm
  }
  stage("Build Process"){
    echo 'Building...'
  }

  stage("Test Analysis "){
      echo 'Test Analyzing...'
    }

  stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarScanner';
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}