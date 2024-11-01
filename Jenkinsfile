pipeline {
  agent any
  stages {
    stage('Hello-proj1') {
        steps {
            echo "hello from Jenkinsfile for proj1"
      }
    }
    stage('fix branch build') {
        when {
            branch "fix-*"
        }
        steps {
            sh '''
            echo "This stage build only fix branches"
            '''
        }
    }
    stage('PR build branch') {
        when {
            branch "PR-*"
        }
        steps{
            sh '''
            echo "This build only PR's "
            '''
        }
    }   
  }
}