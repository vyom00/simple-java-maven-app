node {
    stage('build')
    node {
        checkout scm
        sh 'mvn install package'
    }
    stage('test') {
        try { 
            sh 'mvn test'
        }
        finally {
            junit '**/target/*.xml'
        }
    }
}   
