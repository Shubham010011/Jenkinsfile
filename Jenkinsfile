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
                bat 'if not exist "%USERPROFILE%\\Desktop\\JenkinsDeploy" mkdir "%USERPROFILE%\\Desktop\\JenkinsDeploy"'
                bat 'copy target\\*.jar %USERPROFILE%\\Desktop\\JenkinsDeploy'

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
