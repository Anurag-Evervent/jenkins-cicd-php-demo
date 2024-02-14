pipeline {

    agent {label 'php'}

    stages {
        stage('SCM Checkout') {
            steps {
                // Checkout your source code from version control
                 echo 'SCM'
                git 'https://github.com/Anurag-Evervent/jenkins-cicd-php-demo.git'
            }
        }
    }
}
