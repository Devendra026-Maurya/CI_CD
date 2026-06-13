pipeline {
    agent any

    stages {
        stage('Install') {
            steps {
                 sh 'npm install'
            }
        }

        stage('Bluid') {
            steps {
                echo 'npm run bluid'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy Stage'
                sh '''
                cp -r dist/* /var/www/html/
                sudo systemctl restart nginx
                '''
            }
        }
    }
}