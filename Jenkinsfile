pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Starting build'
            }
        }
        stage('Test') {
            steps {
                bat '''
                echo Running pytest

                call .venv\\Scripts\\activate

                pytest
                '''
            }
        }
        stage('Deploy') {
            steps {
                echo 'In this step, we deploy our project'
                echo 'Depending on the context, we may publish the project artifact or upload pickle files'
            }
        }
    }
}
