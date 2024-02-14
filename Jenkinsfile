pipeline {

    agent {label 'php'}

    stages {
        stage('Pull Code') {
            steps {
                // Checkout code from the GitHub repository
                checkout([$class: 'GitSCM', branches: [[name: '*/Development']], 
                          userRemoteConfigs: [[url: 'https://github.com/Anurag-Evervent/jenkins-cicd-php-demo.git']]])
            }
        }
    }
}
