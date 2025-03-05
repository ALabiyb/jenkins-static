pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/ALabiyb/jenkins-static.git'
            }
            steps {
                sh '''
                    docker images
                '''
            }

            post {
                success {
                    echo "Pipeline completed successfully!"
                }          
                failure {
                    echo "Pipeline failed!"
                }
            }
        }
    }
}
