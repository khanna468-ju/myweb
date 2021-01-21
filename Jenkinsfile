pipeline {
  agent any
  environment {
     PATH=/usr/local/apache-maven/apache-maven-3.6.3/bin:$PATH
  }
    stages {
      stage('git checkout') {
       steps {
        git credentialsId: 'gitaccess', url: 'https://github.com/khanna468-ju/myweb.git'
       }
    }
      stage('buildt') {
       steps {
        sh " mvn clean install "
       }
    }
  }
}
