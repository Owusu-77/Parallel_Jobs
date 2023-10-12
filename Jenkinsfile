pipeline {
    agent any
    stages {
        stage('1-Clonecode') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/Owusu-77/Parallel_Jobs.git']]])
            }
        }
       parallel {
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
       }
        stage('4-Security_Check') {
            steps {
                sh 'bash -x /var/lib/jenkins/workspace/Parallel_Job/pipeline.sh'
            }
        }
    }
}













