pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        sh 'rm -rf /Users/Shared/Jenkins/Home/workspace/spring-petclinic*'
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