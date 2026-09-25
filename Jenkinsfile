pipeline {
    agent any

    stages {

        stage('Check Environment') {
            steps {
                sh 'python3 --version'
                sh 'pip3 --version'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'pip3 install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                sh 'pytest'
            }
        }

        stage('Build') {
            steps {
                sh 'mkdir -p build'
                sh 'cp app.py build/'
                sh 'cp requirements.txt build/'
            }
        }
    }
}