pipeline {
  agent any
    stages {
      stage('git checkout') {
       steps {
        git credentialsId: 'gitaccess', url: 'https://github.com/khanna468-ju/myweb.git'
       }
    }
  }
}
