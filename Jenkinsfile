pipeline{
    agent any
    stages{
        stage('1-firststage'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-id', url: 'https://github.com/etechDevops/teamwork.git']]])
            }
        }
        stage('2-systemcheck'){
            steps{
                sh 'free -g'
            }
        }
    }
}