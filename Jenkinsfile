pipeline {
    agent any

    stages {
        stage('Build and Package') {
            steps {
                script {
                    sh './build.sh'
                }
            }
        }

        stage('Run the Spring Boot App') {
            steps {
                script {
                    sh 'java -jar target/Spring-Boot-Web-App.jar &'
                    sleep 10
                }
            }
        }

        stage('Cleanup') {
            steps {
                script {
                    sh 'pkill -f "java -jar"'
                }
            }
        }
    }

}

