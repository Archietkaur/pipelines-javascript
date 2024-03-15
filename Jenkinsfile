node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarQube';
    withSonarQubeEnv('sonarqube') {
      sh "${scannerHome}/sonar-scanner"
    }
  }
}
