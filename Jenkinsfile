pipeline {
    agent any
    environment {
        python="C:\\Program Files\\Python313\\python.exe"
    }
    stages {
        stage('Build') {
            steps {
                bat "${python} code.py"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
