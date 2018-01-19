pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/lokeshjpt/spring-petclinic.git', branch: 'master', changelog: true, poll: true)
      }
    }
    stage('build') {
      steps {
        sh 'mvn -e -X clean install'
      }
    }
  }
}