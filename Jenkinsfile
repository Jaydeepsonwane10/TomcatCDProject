pipeline {

    agent any

    stages {

        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Deploy') {
            steps {
                bat '''
                echo Deploying WAR to Tomcat...

                copy /Y "target\\tomcat-cd-project.war" "C:\\Users\\Administrator\\Desktop\\jaydeep\\server\\apache-tomcat-10.1.42\\apache-tomcat-10.1.42\\webapps\\"

                echo Deployment completed.
                '''
            }
        }
    }
}