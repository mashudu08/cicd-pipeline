pipeline {
    agent any

    stages {
        
            stage('Build') {
            steps {
                // Build the Spring Boot application using Maven
                script {
                    sh "mvnw clean install"
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

