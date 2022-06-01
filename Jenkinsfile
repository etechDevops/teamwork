pipeline{
    agent any
    stages{
        stage('1-firststage'){
            steps{
                sh 'lscpu'
            }
        }
        stage('2-systemcheck'){
            steps{
                sh 'free -g'
            }
        }
    }
}