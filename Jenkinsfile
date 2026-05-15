pipeline {
    agent { label 'dev' }

    stages {

        stage('Clone Code') {
            steps {
                git branch: 'dev',
                url: 'https://github.com/saraswatilamture/assignment-5-repo.git'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                sudo cp index.html /var/www/html/index.html
                sudo systemctl restart httpd
                '''
            }
        }
    }
}
