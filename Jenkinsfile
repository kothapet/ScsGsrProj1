pipeline {
  agent any
  stages {
    stage('hello') {
      steps {
        echo "hello from Jenkinsfile"
      }  
    }  
    stage('for fix branch') {
      when {
        branch "fix-*"
      }  
      steps {
        cat README.md
      }  
    }  
    stage('for PR') {
      when {
        branch "PR-*"
      }  
      steps {
        echo "This only runs for PRs"
      }  
    }  
  }
}
