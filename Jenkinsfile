pipeline {
     agent any
     stages{
      stage('Checkout Code from GitHub Repository'){
        steps{
         git 'https://github.com/Shobika/DVWA.git'
        }
      }
      stage('SonarQube Analysis') {
       environment {
          SCANNER_HOME = tool 'SonarScan'
        }
           steps {
          withSonarQubeEnv('Vuln') {
          sh "${SCANNER_HOME}/bin/sonar-scanner"
      }
    }
    }
    }
}


