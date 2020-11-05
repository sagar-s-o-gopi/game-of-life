pipeline{
    agent {label 'SAGARLINUX'}
    triggers {pollscm ('* * * * *')}
     stages{
        stage ('clone and compile'){
            steps {
                url: 'https://github.com/sagar-s-o-gopi/game-of-life.git'
                sh 'mvn  package'
            }
            
        }
    }
}
