node {
    stage('build') {
        checkout scm
        sh 'mvn install package'
    }
    stage('test') {
        test { 
            sh 'mvn test'
        }
        publish {
            junit '**/target/**/*.xml'
        }
    }
}  
