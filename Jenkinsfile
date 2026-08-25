pipeline {
    agent any

    stages {
        stage('Docker Build') {
            steps {
                echo 'in branch production'
                echo 'Checking Docker version'
                sh 'docker --version'

                echo 'Building Docker image'
                sh 'docker build -t myapp .'
            }
        }

        stage('Docker Run') {
            steps {
                echo 'Creating container'
                sh 'docker run myapp'
            }
        }
    }
}
