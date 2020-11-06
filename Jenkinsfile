node ('SAGARLINUX'){
    stage ('scm'){
        git branch: 'master', url: 'https://github.com/sagar-s-o-gopi/game-of-life.git'
    }
    stage ('build'){
        sh 'mvn package'
    }

}
