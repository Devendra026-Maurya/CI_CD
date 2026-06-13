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
                echo 'npm run build'
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