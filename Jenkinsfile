pipeline{
    agent any

    environment{
        PIP_TARGET = './.venv-packages'
        PYTHONPATH = './.venv-packages'
    }

    stages{
        stage('install dependencies'){
            steps{
                sh 'pip install -target=$PIP_TARGET -r requirements.txt'
            }
        }

        stage('Run Test'){
            steps{
                sh 'pytest test.py'
            }
        }
    }
}