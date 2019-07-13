pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mvn install package' 
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true 
            }
        }
    }
}
