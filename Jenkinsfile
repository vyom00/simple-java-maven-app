node {
    stage('build') {
        checkout scm
        sh 'mvn install package'
    }
    stage('test') {
        try { 
            sh 'mvn test'
        }
        publish {
            junit '**/target/**/*.xml'
        }
    }
}  
