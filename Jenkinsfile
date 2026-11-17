pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning repository from GitHub...'
                checkout scm
            }
        }

        stage('File Verification') {
            steps {
                echo 'Verifying core files (index.html, style.css, script.js)...'
                script {
                    if (isUnix()) {
                        sh 'test -f index.html && test -f style.css && test -f script.js'
                    } else {
                        bat 'if exist index.html if exist style.css if exist script.js (exit 0) else (exit 1)'
                    }
                }
                echo 'All required website files are verified.'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying static website...'
                // Example deployment commands (customize based on your target server):
                // For Nginx / Apache:
                // sh 'cp -r * /var/www/html/'
                // For AWS S3:
                // sh 'aws s3 sync . s3://your-portfolio-bucket --exclude ".git/*" --exclude "Jenkinsfile"'
                echo 'Website deployed successfully!'
            }
        }
    }

    post {
        success {
            echo 'CI/CD Pipeline finished successfully.'
        }
        failure {
            echo 'Pipeline encountered an error. Please inspect logs.'
        }
    }
}
