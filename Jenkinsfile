pipeline {
    agent { label 'SAGARLINUX' }
    triggers { upstream(upstreamProjects: 'job-1', threshold: hudson.model.Result.SUCCESS) }
    stages{
        stage('scm') {
            steps {
                git branch: 'declarative',
                url: 'https://github.com/sagar-s-o-gopi/game-of-life.git'  
            }
        }
        stage('package'){
            steps {
                sh 'mvn package'
                input 'can i proceed to next step'
                archiveArtifacts 'gameoflife-web/target/*.war'
            }
        }
    }
}