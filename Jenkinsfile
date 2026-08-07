pipeline {
    agent {
        label 'PRJ2'
    }

    stages {
        stage('Checkout') {
            steps {
                deleteDir()
                withCredentials([gitUsernamePassword(credentialsId: 'github-creds', gitToolName: 'Default')]) {
                    sh '''
                        git clone https://github.com/Suit4Noah/taskflow.git
                        cd taskflow
                        git checkout main
                    '''
                }
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }
    }
}