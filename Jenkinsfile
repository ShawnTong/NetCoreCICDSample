pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat 'dotnet build -c Debug'
      }
    }
    stage('Test') {
      steps {
        echo 'Test Placeholder'
      }
    }
    stage('Publish') {
      steps {
        bat 'dotnet publish -c Release'
      }
    }
    stage('Archieve') {
      steps {
        bat 'rmdir /s /q C:\\Package'
        bat 'md C:\\Package'
        bat 'xcopy /e /y NetCoreCICDSample\\bin\\Release\\netcoreapp2.2\\publish C:\\Package'
      }
    }
  }
}