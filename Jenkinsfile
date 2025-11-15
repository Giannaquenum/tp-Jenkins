pipeline {
    agent any

    environment {
        DOCKER_IMAGE = 'mon-tp-python'
    }

    stages {

        stage('Test Docker') {
            steps {
                sh 'which docker'
                sh 'docker --version'
                sh 'echo "Salut Gianna ! Docker fonctionne !"'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh "docker build -t ${DOCKER_IMAGE} ."
            }
        }

        stage('Run Python Script') {
            steps {
                sh "docker run --rm -v ${env.WORKSPACE}:/app -w /app ${DOCKER_IMAGE} python app.py"
            }
        }

    }
}
