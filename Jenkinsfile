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
                    git branch: 'master', credentialsId: 'github', url: 'https://github.com/manikandan2297/new'
                }
        }stage(" Maven Clean Package"){
      def mavenHome =  tool name: "Maven", type: "maven"
      def mavenCMD = "${mavenHome}/bin/mvn"
      sh "${mavenCMD} clean package"
    }

    }
}   
