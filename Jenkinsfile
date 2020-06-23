pipeline{
  agent any
   stages{
      stage("code quality"){
          agent{docker'maven:3-alpine'}
          steps{
              sh  '''
              mvn sonar:sonar \
      -Dsonar.projectKey=hari \
      -Dsonar.host.url=http://18.191.223.68:9000 \
      -Dsonar.login=050cafadf583ccda14e9fc88356431afac41a56e
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
