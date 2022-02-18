pipeline {
     agent any
     stages{
      stage('Checkout Code from GitHub Repository'){
        checkout scm
      }
      stage('SonarQube Analysis') {
          def scannerHome = tool 'SonarScanner';
           steps {
          withSonarQubeEnv('Vuln') {
          sh "${scannerHome}/bin/sonar-scanner"
      }
    }
    }
    }
    }


