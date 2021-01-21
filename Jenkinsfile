pipeline {
  agent any
  environment {
     PATH= "/usr/local/apache-maven/apache-maven-3.6.3/bin:$PATH"
  }
    stages {
      stage('git checkout') {
       steps {
        git credentialsId: 'gitaccess', url: 'https://github.com/khanna468-ju/myweb.git'
       }
    }
      stage('build') {
       steps {
        sh " mvn clean install "
       }
    }
      stage('deploy') {
       steps {
        sshagent(['ec2-user']) {
   sh "scp -o StrictHostKeyChecking=no target/myweb-0.12.0.war ec2-user@172.31.3.103:/opt/tomcat/webapps"
}
       }
    }
  }
}
