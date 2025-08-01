pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/Rijomathewjohn/SRD.git'
            }
        }
        stage('Deploy to Apache') {
            steps {
                echo 'Deploying files...'
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
