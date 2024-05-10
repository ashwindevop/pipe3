pipeline {
 agent any

  tools {
     maven  "jenkin-maven"
        }


  stages {
      stage('scm') {
            steps {
               git 'https://github.com/ashwindevop/mvnwar16april.git'
                     }
             }

 stage('build') {
     steps {
                sh "mvn clean package"
               }
        }
          
stage('deploy') {
  steps {
      sh " scp  /var/lib/jenkins/workspace/pipe8/target/myweb2.war  192.168.10.32:/opt/apache-tomcat-8.5.100/webapps"
          }
               }
          }
}
