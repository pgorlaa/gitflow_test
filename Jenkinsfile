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
        input 'Deploy to Convox?'
        sh 'echo Deploy dev test a'
        // sh 'git flow release start release'
      }
    }

    stage('Release') {
      steps {
          sh 'echo release'
      }
    }

    stage('Tag') {
      when {
        expression { env.BRANCH_NAME == 'master' }
      }
      steps {
        sh 'echo masteeeeer'
      }
    }
  }
}