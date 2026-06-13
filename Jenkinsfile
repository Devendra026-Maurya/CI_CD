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
                sh 'npm run build'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy Stage'
                sh '''
                sudo cp -r dist/* /var/www/html/
                sudo systemctl restart nginx
                '''
            }
        }
    }
}