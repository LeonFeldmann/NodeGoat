node {
  stage('SCM') {
    git 'https://github.com/LeonFeldmann/NodeGoat'
  }
  stage('SonarQube analysis') {
    def scannerHome = tool 'SonarScanner 4.0';
    withSonarQubeEnv('Sonarqube Server') { // If you have configured more than one global server connection, you can specify its name
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}
