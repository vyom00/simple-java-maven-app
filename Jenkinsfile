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
        properties([parameters([string(defaultValue: 'Testing, qa, Dev', description: '', name: 'DEVPLOY_ENV', trim: false)])])
    }
} 
