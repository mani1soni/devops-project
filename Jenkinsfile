pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh "sudo docker build -t web-server ."
            }
        }
        stage('Deploy') { 
            steps {
                sh "sudo docker run -itd -p 80:80 web-server"
            }
        }
    }
}
