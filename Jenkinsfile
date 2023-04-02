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
                sh '/usr/local/bin/docker-compose up -d --build'
                sh 'cat/etc/letsencrypt/live/blog.erdogansahin.net/fullchain.pem > /var/lib/jenkins/workspace/github-hook/example.txt'
                echo 'it works111'                
            }
        }
    }
}