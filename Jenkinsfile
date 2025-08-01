pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Rijomathewjohn/SRD.git'
            }
        }

        stage('Deploy to Apache') {
            steps {
                sh '''
                    sudo cp -r * /var/www/html/
                    sudo systemctl restart apache2
                '''
            }
        }
    }
}

