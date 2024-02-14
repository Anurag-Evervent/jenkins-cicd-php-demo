pipeline {
    agent {
        label 'ph'
    }

    stages {
        stage('Pull Code') {
            steps {
                // Checkout code from the GitHub repository
                checkout([$class: 'GitSCM', branches: [[name: '*/Development']], 
                          userRemoteConfigs: [[url: 'https://github.com/Anurag-Evervent/jenkins-cicd-php-demo.git']]])
            }
        }
    }

    post {
        always {
            // Clean up resources or do any other necessary post-processing steps
            echo "Pipeline execution completed."
        }
    }
}
