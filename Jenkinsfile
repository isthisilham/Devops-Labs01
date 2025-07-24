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
                echo 'Menjalankan program...'
                sh 'python3 main.py'
            }
        }

        stage('Test') {
    steps {
        echo 'Menjalankan test...'
        sh '''
            pip install --upgrade pip setuptools
            pip install pytest
            pytest tests/
        '''
    }
}
    }
}
