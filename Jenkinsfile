pipeline{
    agent any

    stages{
        stage('install dependencies'){
            steps{
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Run Test'){
            steps{
                sh 'pytest test.py'
            }
        }
    }
}