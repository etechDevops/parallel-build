pipeline {
    agent any

    stages {
        stage('codecheckout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-id', url: 'https://github.com/etechDevops/parallel-build.git']]])
            }
        }
        stage('action1 and action2'){
            echo 'we check'
            parallel{
                stage('action1'){
                    steps{
                        echo 'action1'
                    }
                }
                stage('action2'){
                    steps{
                        echo 'action2'
                    }
                }
            }
        }
        stage('stop-here'){
            steps{
                echo 'last step'
            }
        }
    }
}
