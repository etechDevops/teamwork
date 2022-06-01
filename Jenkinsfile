pipeline{
    agent any
    stages{
        stage('1-git-clone'){
            steps{
            checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-id', url: 'https://github.com/etechDevops/teamwork.git']]])
            }
        }
        stage('2-cpuinfo'){
            steps{
                sh 'lscpu'
            }
        }
        stage('3-securityscanner'){
            steps{
                sh 'bash /var/lib/jenkins/workspace/testgroup-level-ci/security.sh'
            }
        }
    }
}
