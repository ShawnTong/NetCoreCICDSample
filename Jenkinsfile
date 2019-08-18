pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat(script: 'dotnet build -c Debug', returnStatus: true)
      }
    }
    stage('Test') {
      steps {
        echo 'Test Placeholder'
      }
    }
    stage('Archieve') {
      steps {
        bat 'rmdir /s /q C:\\Package'
        bat 'md C:\\Package'
        bat 'xcopy /e /y NetCoreCICDSample\\bin\\Release\\netcoreapp2.2\\publish C:\\Package'
      }
    }
    stage('Deploy') {
      steps {
        bat(script: 'dotnet C:\\Package\\NetCoreCICDSample.dll', returnStatus: true)
      }
    }
  }
}