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
        sh 'git flow release start release'
      }
    }

    stage('Tag') {
      when {
        expression { env.BRANCH_NAME == 'master' }
      }
      steps {
        sh ''
      }
    }

    stage('deployment') {
        input 'Do you approve deployment?'
    }
  }
}