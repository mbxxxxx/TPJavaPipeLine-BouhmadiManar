pipeline {
    agent {
        docker {
            image 'maven:3.9.6-eclipse-temurin-17'
            args '-v /root/.m2:/root/.m2'
        }
    }

    stages {
        stage('Checkout') {
            steps {
                sh 'rm -rf *'
                sh 'git clone https://github.com/mbxxxxx/TPJavaPipeLine-BouhmadiManar.git'
            }
        }

        stage('Build') {
            steps {
                dir('TPJavaPipeLine-BouhmadiManar/java-maven/maven') {
                    sh 'mvn clean package'
                    sh 'java -jar target/maven-0.0.1-SNAPSHOT.jar'
                }
            }
        }
    }
}
