pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mvn' 
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true 
            }
        }
    }
}
