pipeline {
    agent { label 'agent' }
    tools {
        jdk 'Java17'
        maven 'Maven3'
    }
     stages{
        stage("Cleanup Workspace"){
                steps {
                cleanWs()
                }
        }
         stage("Checkout from SCM"){
                steps {
                    git branch: 'main', credentialsId: 'github', url: 'https://github.com/manikandan2297/new/tree/main'
                }
        }
    }
}   
