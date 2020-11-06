pipeline {
    agent { label 'SAGARLINUX' }
    triggers { upstream(upstreamProjects: 'job1', threshold: hudson.model.Result.SUCCESS) }
    stages{
        stage('scm') {
            steps {
                git branch: 'declarative',
                url: 'https://github.com/jenkinsci/jenkins.git'
            }
        }
        stage('package'){
            steps {
                sh 'mvn package'
            }
        }
    }
}