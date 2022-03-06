pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                echo 'Hello Build'
            }
        }
        stage('test') {
            steps {
                echo 'Hello test'
            }
        }
        stage('deploy') {
            steps {
                echo 'Hello deploy'
            }
        }
    }
    post{
        always{
            emailext body: 'Syntax Error', subject: 'Build Failed', to: 'shailesh2405@gmail.com'
        }
    }
}
