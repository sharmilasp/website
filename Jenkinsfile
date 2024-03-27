pipeline {
    agent none
    stages {
        stage('Build and Publish Website') {
            agent{
                label 'slave-2'
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
