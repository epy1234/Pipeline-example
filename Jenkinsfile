pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build Process'
            }
        }
        stage('Run') {
            steps {
                echo 'Run Process'
            }
        }
    }
    post {
        always {
            emailext body: 'The exercise work fine!', recipientProviders: [[$class: 'DevelopersRecipientProvider'],
            [$class: 'RequesterRecipientProvider']], subject: 'Jenkins works with Epy gmail'
        }
    }
}
