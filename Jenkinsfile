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
        
        stage('Copy Files and Restart Nginx') {
            steps {
                // Copy files and folders
                sh "cp -r /home/ubuntu/workspace/nch_Pipeline_project_Development/* /var/www/html/workspace/nch_Pipeline_project_Development"
                
                // Restart Nginx
                sh "sudo systemctl restart nginx"
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
