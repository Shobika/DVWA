pipeline {
     agent any
      stage('Checkout Code from GitHub Repository'){
        checkout scm
      }
      stage('SonarQube Analysis') {
          def scannerHome = tool 'SonarScanner';
          withSonarQubeEnv() {
          sh "${scannerHome}/bin/sonar-scanner"
      }
    }