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
       properties([parameters([choice(choices: ['TESTING', 'PROD', 'QA'], description: '', name: 'DEPLOY_ENV')])])
       input 'do you wan to deploy ${params.DEPLOY_ENV}?'
       echo "Will deploy to ${params.DEPLOY_ENV}"
    }
}
