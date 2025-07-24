pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        git branch: 'main', url: 'https://github.com/isthisilham/Devops-Labs01.git'
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
    echo 'Menjalankan test...'
    sh '''
      python3 -m pip install pytest
      pytest tests/
    '''
  }
}

  }
}
