pipeline{
    agent any
     stages {
        stage('Git Checkout') {
          steps {
            echo "Checkout"
            checkout scm
          }
        }
        stage('Building Docker Image'){
            steps{
                echo 'Testing'
                sh 'docker --version'
            }
        }
        stage('Deploy'){
            steps{
                sh "docker build . -t upgrad-app\${BUILD_NUMBER}"
            }
        }
     }
}
