pipeline {
    agent any
    environment {
        python='"C:\\Program Files\\Python313\\python.exe"'
    }
    stages {
        stage('Build') {
            steps {
                bat "${python} code.py"
            }
        }
        stage('Parallel tasks') {
                           steps {
                    parallel (
                    "TaskOne" : {
                        echo 'task one stuff part 1'
                        echo 'task one stuff part 2'
                        echo 'task one stuff part 3'
                    },
                    "TaskTwo" : {
                        echo 'tasl two stuff part 1'
                        echo 'tasl two stuff part 2'
                    }
                    )
            }

        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
