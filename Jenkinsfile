pipeline {
    agent any

    environment {
        FIREBASE_TOKEN = credentials('FIREBASE_TOKEN')
    }

    stages {
        stage('Install Firebase CLI') {
            steps {
                sh 'curl -sL https://firebase.tools | bash'
            }
        }

        stage('Deploy to Testing') {
            steps {
                sh 'firebase deploy --project final-exam-testing --token $FIREBASE_TOKEN'
            }
        }

        stage('Deploy to Staging') {
            steps {
                sh 'firebase deploy --project final-exam-staging --token $FIREBASE_TOKEN'
            }
        }

        stage('Deploy to Production') {
            steps {
                sh 'firebase deploy --project final-exam-production-8e528 --token $FIREBASE_TOKEN'
            }
        }
    }
}

