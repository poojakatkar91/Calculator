node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def mvn = tool 'Default Maven';
    withSonarQubeEnv(SonarQube) {
      sh "${mvn}/bin/mvn sonar:sonar"
    }
  }
}
