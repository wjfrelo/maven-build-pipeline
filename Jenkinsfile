pipeline {
  agent any
  stages {
    stage('') {
      steps {
        tool(type: 'maven', name: 'my-maven')
      }
    }

    stage('Pull Github') {
      steps {
        git(url: 'git@github.com:wjfrelo/maven-build-pipeline.git', branch: 'main', credentialsId: '7562e52145921fe8f2eaec2d644c91aae08c9a47', poll: true, changelog: true)
      }
    }

    stage('Build') {
      steps {
        sh 'sh \'mvn compile\''
      }
    }

    stage('Unit Test') {
      steps {
        sh 'sh \'mvn test\''
      }
    }

  }
}