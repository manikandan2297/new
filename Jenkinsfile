pipeline{
    agent{
        label "jenkins-agent"
    }
    tools{
        jdk 'java17'
        maven 'maven3'
    }
    stages{
        stage("Cleanup workspace"){
            steps{
                cleanWs()
            }
        }
    }
    stages{
        stage("Checkout from SCM"){
            steps{
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/manikandan2297/new'
            }
        }
    } 
}
