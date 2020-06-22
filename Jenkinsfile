pipeline{
  agent any
  stages{
      stage("code quality"){
          steps{
              sh '''
              mvn sonar:sonar \
  -Dsonar.projectKey=testing \
  -Dsonar.host.url=http://13.59.45.195:9000 \
  -Dsonar.login=40975f5f5c4ca014176e9e9f027e753039721cbe
                 '''
          }
      }
      stage("code build"){
          agent{docker'maven:3-alpine'}
            steps{
                sh 'mvn clean package'
            }
      }
  }
}
