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
        sh '/Users/Shared/apache-maven-3.5.2/bin/mvn -e -X clean install'
      }
    }
  }
}