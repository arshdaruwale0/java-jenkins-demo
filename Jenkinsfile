pipeline {
    agent any

    environment {
        PATH = "/opt/homebrew/opt/openjdk/bin:/opt/homebrew/bin:/usr/bin:/bin:/usr/sbin:/sbin"
        JAVA_HOME = "/opt/homebrew/opt/openjdk"
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Run') {
            steps {
                sh 'java -cp target/classes Hello'
            }
        }
    }
}
