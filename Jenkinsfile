node {
    stage('Preparation') {
        catchError(buildResult: 'SUCCESS') {
            sh 'docker stop samplerunning'
            sh 'docker rm samplerunning'
        }
    }
    stage('Build') {
        build '.NETAppBuild'
    }
    stage('Results') {
        build 'test.NETApplicationServer'
    }
}