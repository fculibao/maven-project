pipeline {
    agent any
    stages{
        stage('Build'){
            def mav_version = 'maven-3.5.4'
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
