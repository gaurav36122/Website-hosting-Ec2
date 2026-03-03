pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                git branch: 'main', 
                    url: 'https://github.com/gaurav36122/Website-hosting-Ec2.git'
            }
        }

        stage('Deploy to S3') {
            steps {
                sh 'aws s3 sync . s3://amzn-demo-0111'
            }
        }
    }
}
