pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
          sh 'echo Test'
      }
    }

    stage('Deploy dev') {
      when {
        expression { env.BRANCH_NAME == 'develop' }
      }
      steps {
        sh 'echo Deploy dev test a'
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