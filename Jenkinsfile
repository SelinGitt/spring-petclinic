node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def mvn = tool 'Default Maven';
    withSonarQubeEnv() {
      sh "./mvnw clean verify sonar:sonar -Dsonar.projectKey=test -Dsonar.projectName='spring-petclinic' -Dsonar.host.url=http://localhost:9000 -Dsonar.login=sqp_2e9f6ec4cdd43706ee8cac8d1a4849e329b52392
"
    
  }
}
