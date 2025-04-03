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

                python -m pip install --upgrade pip
                python -m pip install -r requirements.txt

                python -m pytest
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
