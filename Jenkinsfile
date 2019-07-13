node {
    stage('build')
    node {
        checkout scm
        sh 'mvn install package'
    }
}
