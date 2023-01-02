node {
    stage('Cont.Download') {
    git 'https://github.com/venkat9822891/new-proj.git'
                           }
    stage('Cont.Build') {
    sh 'mvn package'
                        }
    stage('Cont.Deployment') {
    deploy adapters: [tomcat8(credentialsId: '4c52b258-81c6-4001-9a55-63f6487b9c55', path: '', url: 'http://35.154.245.132:8080/')], contextPath: '/test-icici', war: '**/*.war'
                              }
}
