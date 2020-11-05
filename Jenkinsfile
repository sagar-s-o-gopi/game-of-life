node ('SAGARLINUX'){
    stage ('scm'){
       git branch: 'master', url ='https://github.com/wakaleo/game-of-life.git'
    }
    stage('build'){
        sh 'mvn package'
    }
}

