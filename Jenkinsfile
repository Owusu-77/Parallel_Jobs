pipeline {
    agent any
    stages {
        stage('1-Clonecode') {
            steps {
               checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'Team7-git-id', url: 'https://github.com/Owusu-77/Parallel_Jobs.git']]) 
                
            }
        }
        stage('2-Build') {
            steps {
                sh 'df -h'
            }
        }
        stage('3-RunTest') {
            steps {
                sh 'lscpu'
            }
        }
         stage('4-Security_Check') {
            steps {
              sh 'bash -x /var/lib/jenkins/workspace/Parallel_Job/pipeline.sh  
            }
    }
    }
}












