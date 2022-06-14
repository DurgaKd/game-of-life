node('JDK11') {
    stage('scm'){
        git branch: 'master' , url: 'https://github.com/wakaleo/game-of-life.git'
    }
    stage('build'){
        sh 'mvn package'
    }
    stage('postbuild'){
        junit '**/TEST-*.xml'
        archive '**/*.war'
    }
}