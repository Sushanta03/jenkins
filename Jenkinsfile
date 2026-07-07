pipeline {
    agent any

    stages {
        stage('Pull Latest Code') {
            steps {
                sh '''
                cd /path/to/git-content
                git checkout develop
                git pull origin develop
                '''
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                sudo cp /path/to/git-content/index.html /var/www/html/index.html
                '''
            }
        }
    }
}
