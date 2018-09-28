pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
          sh 'Test'
      }
    }

    stage('Tag') {
      when {
        expression { env.BRANCH_NAME == 'dev' }
      }
      steps {
        sh 'Deploy dev test'
      }
    }

    stage('Tag') {
      when {
        expression { env.BRANCH_NAME == 'master' }
      }
      steps {
        sh 'Tag test'
      }
    }
  }
}