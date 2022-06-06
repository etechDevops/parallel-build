pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('action1 and action2'){
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
