pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        tool(type: 'maven', name: 'my-maven')
      }
    }

    stage('Pull Github') {
      steps {
        git(url: 'git@github.com:wjfrelo/maven-build-pipeline.git', branch: 'main', credentialsId: 'wjfrelo', poll: true, changelog: true)
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