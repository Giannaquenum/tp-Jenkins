pipeline {
    agent {
        docker {
            image 'python:3.14-alpine'
            args '-u root:root'
        }
    }
    stages {
        stage('Test Docker') {
            steps {
                sh 'python --version'
                sh 'echo "Salut Gianna ! Docker fonctionne !"'
            }
        }
        stage('Run Python Script') {
            steps {
                sh 'python app.py'
            }
        }
    }
}

