pipeline{
    agent any
    stages {
        stage('Build'){
            steps{
                build 'PES1UG21CS123-1'
                sh 'g++ PES1UG21CS123.cpp -o output'
            }
        }
        stage('Test'){
            steps{
                sh './output1'
            }
        }
        stage('Deploy'){
            steps{
                echo 'deploy'
            }
        }
    }
    post{
        failure{
            error 'Pipeline failed'
        }
    }
}