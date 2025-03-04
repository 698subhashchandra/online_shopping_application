pipeline {
    agent { label "dev"};

    stages {
        stage('Code') {
            steps {
                echo 'Clonning the Code'
                git url: "https://github.com/698subhashchandra/online_shopping_application.git", branch: "main"
            }
        }
        stage('Build') {
            steps {
                echo 'Building ......'
                sh "docker build -t online_shop ."
            }
        }
        stage('Test') {
            steps {
                echo 'Testing ....'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying .....'
                sh "docker compose up --build online_shop"
            }
        }
    }
}
