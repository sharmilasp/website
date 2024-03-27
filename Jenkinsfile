pipeline {
    agent none
    stages {
        stage('Build and Publish Website') {
            agent{
                label 'slave2'
            }
            when {
                branch 'develop'
            }
            steps {
                sh 'sudo docker build -t devimage .'      
            }
        }
    }
}
