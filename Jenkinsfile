pipeline{
    agent any
    stages{
        stage('1-git-clone'){
            steps{
            checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-id', url: 'https://github.com/etechDevops/teamwork.git']]])
            }
        }
    }
}
