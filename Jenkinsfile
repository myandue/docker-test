pipeline {
    agent any
    stages {
        stage('pull') {
            steps {
                git fetch
                git pull origin main
            }
        }
        stage('build') {
            steps {
                echo 'building the application...'
                npm run build
            }
        }
        stage('deploy') {
            steps {
                echo 'deploying the application...'
                pm2 restart
            }
        }
    }
}
