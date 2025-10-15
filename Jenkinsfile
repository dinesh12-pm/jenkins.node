pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/dinesh12-pm/jenkins.node.git
            }
        }

        stage('Compile') {
            steps {
                echo 'Compiling Java project...'
                bat 'javac src\\Main.java -d bin'
            }
        }

        stage('Run') {
            steps {
                echo 'Running Java project...'
                bat 'java -cp bin Main'
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
