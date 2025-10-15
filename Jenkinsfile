pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/dinesh12-pm/jenkins.node.git
            }
        }

        stage('Build') {
            steps {
                echo 'No build needed for static site.'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying static site...'
                // Copy files to a folder or start a simple Windows web server
                bat 'mkdir C:\\JenkinsStaticDemo'
                bat 'xcopy /E /Y * C:\\JenkinsStaticDemo'
                echo 'Static site deployed to C:\\JenkinsStaticDemo'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
