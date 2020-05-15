node('UBUNTU') {
    stage('scm') {
        git 'https://github.com/wakaleo/game-of-life.git'

    }

    stage('build') {
        sh label: '', script: 'mvn package'
        
        }
    stage('postbuild'){
        archiveArtifacts 'gameoflife-web/target/*.war'
        junit 'gameoflife-web/target/surefire-reports/*.xml'
    }
}
