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
                bat 'mkdir %USERPROFILE%\\Desktop\\JenkinsDeploy'
                bat 'copy target\\*.jar %USERPROFILE%\\Desktop\\JenkinsDeploy'

            }
        }
    
    stages('Deploy'){
        steps{
            echo 'Deploying the Application'
            bat 'Windows command'
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
