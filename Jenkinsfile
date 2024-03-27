pipeline {
    agent none
    stages {
        stage('Build and Publish Website') {
            agent{
                label 'slave-1'
            }
            when {
                    branch 'master'
            }
            steps {
                    sh 'sudo docker rm -f c1'
                    sh 'sudo docker build -t prodimage .'
                    sh 'sudo docker run -itd -p 82:80 --name=c1 prodimage'      
            }
        }
    }
}
