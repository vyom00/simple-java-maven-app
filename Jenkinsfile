node {
    stage('build') {
        checkout scm
        sh 'mvn install package'
    }
    stage('test') {
        try { 
            sh 'mvn test'
        }
        finally {
            junit '**/target/**/*.xml'
        }
    }
    stage('deploy'){
        properties([parameters([string(defaultValue: 'TESTING \\ QA \\ PROD', description: '', name: 'DEVPLOY_ENV', trim: false)])])
    }
} 
