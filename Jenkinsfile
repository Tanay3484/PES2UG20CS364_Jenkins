pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES2UG20CS364-1 main/hello.cpp'
            }
        }

        stage('Test') {
            steps {
                sh './PES2UG20CS364-1'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
    }

    post {
        always {
            script {
                if (currentBuild.result != 'SUCCESS') {
                    echo 'Pipeline failed'
                }
            }
        }
    }
}
