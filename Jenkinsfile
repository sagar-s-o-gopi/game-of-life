pipeline {
    agent { label 'SAGARLINUX' }
    triggers { pollSCM ('* * * * *') }
    stages {
        stage('clone and compile') {
            steps {
                git branch: 'declarative'
                url: 'https://github.com/sagar-s-o-gopi/game-of-life.git'
                sh 'mvn  package'
            }
            
        }
    }
}
