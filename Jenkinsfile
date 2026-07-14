pipeline {
    agent any

    stages {
        stage('Pull Latest Code') {
            steps {
                sh '''
                cd /var/lib/jenkins/git-content
                git config --global --add safe.directory /var/lib/jenkins/git-content
                git pull origin develop
                '''
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                sudo cp /var/lib/jenkins/git-content/index.html /var/www/html/index.html
                '''
            }
        }
    }
}
