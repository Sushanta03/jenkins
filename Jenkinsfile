pipeline {
    agent any

    stages {

        stage('Pull Latest Code') {
            steps {
                sh '''
                cd /root/git-content
                git checkout develop
                git pull origin develop
                '''
            }
        }

        stage('Deploy to Apache') {
            steps {
                sh '''
                sudo cp /root/git-content/index.html /var/www/html/index.html
                '''
            }
        }

    }
}
