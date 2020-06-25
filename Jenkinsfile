pipeline {
                                agent {label 'slave1'}
    stages {
        stage('deployment') {
            steps {
            sh'''
            id
            pwd
            cd /home/ubuntu/
            ls -lrt
            curl -uadmin:APASfQaa9ckVm7xtrFxAepxV1QE -O "http://52.15.72.139:8082//artifactory/project/sparkjava-hello-world-1.0.war"
            cp sparkjava-hello-world-1.0.war /opt/tomcat/webapps/
        
            '''
                }
            }

            stage('testing') {
                steps {
                    sh "echo 'testing'"
                }
            }
                }
        }
