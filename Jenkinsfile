pipeline {
    agent any

    environment {
        DESTINATION = "/var/lib/jenkins/git-content"
    }

    stages {

        stage('Copy Git Content') {
            steps {
                sh '''
                mkdir -p ${DESTINATION}
                cp -rf * ${DESTINATION}/
                '''
            }
        }

        stage('Deploy to Apache') {
            steps {
                sh '''
                sudo cp ${DESTINATION}/index.html /var/www/html/index.html
                '''
            }
        }

    }

    post {
        success {
            echo 'Deployment completed successfully.'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
