pipeline {
    agent any

    stages {

        stage('Pull Latest Code') {
            steps {
                sh '''
                cd /var/lib/jenkins/git-content
                git checkout develop
                git pull origin develop
                '''
            }
        }

        stage('Deploy to Apache') {
            steps {
                sh '''
                cp /var/lib/jenkins/git-content/index.html /var/www/html/index.html
                '''
            }
        }

    }
}
                '''
            }
        }

    }
}
