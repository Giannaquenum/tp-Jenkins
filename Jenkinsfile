pipeline {
    agent { docker { image 'python:3.14-alpine' } }
    stages {
        stage('Test Docker') {
            steps {
                sh 'python --version'
                sh 'echo "Salut Gianna ! Docker fonctionne !"'
            }
        }
    }
}
