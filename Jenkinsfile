pipeline {
    agent any

    stages {
        stage('Install Firebase CLI') {
            steps {
                sh 'curl -sL https://firebase.tools | bash'
            }
        }

        stage('Deploy to Testing') {
            steps {
                sh 'firebase deploy --project final-exam-testing'
            }
        }

        stage('Deploy to Staging') {
            steps {
                sh 'firebase deploy --project final-exam-staging'
            }
        }

        stage('Deploy to Production') {
            steps {
                sh 'firebase deploy --project final-exam-production-8e528'
            }
        }
    }
}
