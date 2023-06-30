
pipeline {
    agent any
          stages {
              stage('checkout') {
                 steps {
                 echo " checkout stage "
                 git branch: 'main', url: 'https://github.com/hariprasadbl/practice.git'
               }
          }

             stage('build') {
                steps {
                 echo " Build stage "
                 sh 'mvn clean package'
                }
          }

            stage('artifactory') {
               steps {
                  echo " artifactory stage "
               }
           }

            stage('deployment') {
               steps {
                  echo " deployement stage "
                  sh 'sudo  cp /home/ubuntu/jenkins/workspace/demo-tomcat/target /opt/tomcat/webapps'
               }
          }

    }
}  
