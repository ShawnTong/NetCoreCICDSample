pipeline {
  agent any
  stages {
    stage('Restore') {
      steps {
        bat(script: 'dotnet restore', returnStatus: true)
      }
    }
  }
}