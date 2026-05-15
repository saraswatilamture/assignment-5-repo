pipeline {
    agent { label 'dev' }

    stages {

        stage('Clone Code') {
            steps {
                deleteDir()

                git branch: 'dev',
                url: 'https://github.com/username/assignment-5-repo.git'
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
