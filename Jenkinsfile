pipeline {
    agent {
        docker {
            image 'alpine'  // Specify the Docker image to use
            args '-it'  // Specify additional Docker run arguments
        }
    }
    stages {
        stage('Run Docker Container') {
            steps {
                sh 'echo "Hello, World!"'
            }
        }
    }
    post {
        always {
            sh 'docker rm -f my-container'  // Remove the Docker container when the job is done
        }
    }
}
