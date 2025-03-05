pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/ALabiyb/jenkins-static.git'

                // Run Maven on a Unix agent.
                sh "docker build -t sample ."

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
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
