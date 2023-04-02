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
                sh 'sudo cat /etc/letsencrypt/live/blog.erdogansahin.net/fullchain.pem > /var/lib/jenkins/workspace/github-hook/nginx/fullchain.pem'
                sh 'sudo cat /etc/letsencrypt/live/blog.erdogansahin.net/privkey.pem > /var/lib/jenkins/workspace/github-hook/nginx/privkey.pem'
                sh '/usr/local/bin/docker-compose up -d --build'
                echo 'it works111'                
            }
        }
    }
}