pipeline {
    agent any

     tools {
        maven 'Maven 3'
        git 'Git'
    }

    stages {
        
            stage('Build and Package') {
            steps {
                // Build the Spring Boot application using Maven
                script {
                    sh './mvnw clean install -DskipTests'
                }
            }
        }

        stage('Run') {
            steps {
                script {
                    sh 'java -jar target/Spring-Boot-Web-App.jar &'
                    sleep 10
                }
            }
        }

        // stage('Cleanup') {
        //     steps {
        //         script {
        //             sh 'pkill -f "java -jar"'
        //         }
        //     }
        // }
    }

}

