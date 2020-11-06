pipeline {
    agent { label 'SAGARLINUX' }
    triggers { upstream(upstreamProjects: 'job-1', threshold: hudson.model.Result.SUCCESS) }
    parameters { string(name: 'DEPLOY_ENV', defaultValue: 'master', description: 'this is for checking') }
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
                archiveArtifacts 'gameoflife-web/target/*.war'
            }
        }
    }
}