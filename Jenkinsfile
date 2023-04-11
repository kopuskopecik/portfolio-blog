pipeline {
    agent any
    environment {
        PATH = "$PATH:/usr/local/bin/docker-compose"
    }
    stages {
        stage('build') {
            steps {
                sh 'pwd'
                sh "cd /var/lib/jenkins/workspace/github-hook"
                sh "docker system prune -a --force"
                sh '/usr/local/bin/docker-compose down'
                sh '/usr/local/bin/docker-compose up -d --build'
                echo 'it works111'                
            }
        }
    }
}









