pipeline {
     agent any
     stages{
      stage('Checkout Code from GitHub Repository'){
        steps{
         git 'https://github.com/Shobika/DVWA.git'
        }
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


