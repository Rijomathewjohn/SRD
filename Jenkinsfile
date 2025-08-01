pipeline {
    agent any
    stages {
        stage('Deploy to Apache') {
            steps {
                echo 'Deploying files to Apache...'
                sh '''
                    rm -rf /var/www/html/*
                    cp -r * /var/www/html/
                '''
            }
        }
    }
    post {
        success {
            echo 'Deployment complete!'
        }
        failure {
            echo 'Deployment failed.'
        }
    }
}
