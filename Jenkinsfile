pipeline {
    agent {label 'JDK11'}
    stages {
        stage ('scm') {
            steps {
                git branch: 'master' , url: 'https://github.com/DurgaKd/game-of-life.git'
            }
        }
        stage ('build') {
            steps {
                sh 'mvn package'
            }
        }
    }
}