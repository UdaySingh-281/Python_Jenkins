pipeline{
    agent any

    stages{
        stage('install dependencies'){
            sh 'pip install -r requirements.txt'
        }

        stage('Run Test'){
            sh 'pytest test.py'
        }
    }
}