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
                sh 'sudo /bin/cp index.html /var/www/html/index.html'
            }
        }
    }
}

