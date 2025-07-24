pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        git 'https://github.com/isthisilham/Devops-Labs01.git'
      }
    }
    stage('Build') {
      steps {
        sh 'echo Menjalankan program...'
        sh 'python3 main.py'
      }
    }
    stage('Test') {
      steps {
        sh 'echo Menjalankan test...'
        sh 'pytest tests/'
      }
    }
  }
}
