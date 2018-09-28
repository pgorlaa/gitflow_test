pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
          sh 'echo Test'
      }
    }

    stage('Tag') {
      when {
        expression { env.BRANCH_NAME == 'dev' }
      }
      steps {
        sh 'echo Deploy dev test'
      }
    }

    stage('Tag') {
      when {
        expression { env.BRANCH_NAME == 'master' }
      }
      steps {
        sh 'echo Tag test'
      }
    }
  }
}