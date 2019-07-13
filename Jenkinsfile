node {
    stage('build')
    node {
        checkout scm
        sh 'mvn install package'
    }
    stage('test')
        sh 'mvn test'
    junit '**/target/*.xml'
}
