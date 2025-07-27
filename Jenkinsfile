pipeline{
    agent {
        docker{
            image 'python:3.10'
        }
    }

    environment{
        PIP_TARGET = './.venv-packages'
        PYTHONPATH = './.venv-packages'
    }

    stages{
        stage('install dependencies'){
            steps{
                sh 'python3 -m pip install -target=$PIP_TARGET -r requirements.txt'
            }
        }

        stage('Run Test'){
            steps{
                sh 'python3 -m pytest test.py'
            }
        }
    }
}