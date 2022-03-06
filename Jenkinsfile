pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M3"
    }
    
    stages {
        stage('build') {
            steps { 
                echo 'Hello Build'
                git branch: 'master',url: 'https://github.com/shailesh2405/demoIDFC.git'

                // Run Maven on a Unix agent.
                bat "mvn -Dmaven.test.failure.ignore=true clean package"
                echo 'Hello Build complete'
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
