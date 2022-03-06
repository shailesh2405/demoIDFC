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
            mail bcc: '', body: 'Jenkins Body', cc: '', from: '', replyTo: '', subject: 'Jenkins test', to: 'neha.ckt05@gmail.com'
        }
    }
}
