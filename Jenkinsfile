pipeline {
    agent any
    stages {
        stage('Build HTML') {
            steps {
                sh 'docker build -t my-html-image .'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker run -d -p 8080:80 --name html-app my-html-image'
            }
        }
    }
}