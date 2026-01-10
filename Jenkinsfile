pipeline {
    agent any

    tools {
        jdk 'JDK8'
        maven 'Maven3'
    }

    stages {

        stage('Build') {
            steps {
                echo 'Building project using Maven'
                bat 'mvn clean package'
                bat 'C:\Users\sharm\OneDrive\Desktop\JenkinsDeploy'
                bat 'copy target\\*.jar C:\ProgramData\Jenkins\.jenkins\workspace\JenkinsDeploy\target'

            }
        }
    
    stage('Deploy'){
        steps{
            echo 'Deploying the Application'
            bat 'echo Application deployed successfully'
        }
    }
}
    post {
        success {
            echo 'Maven build successful'
        }
        failure {
            echo 'Maven build failed'
        }
    }
}
