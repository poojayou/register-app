pipeline {
    agent { A 'Jenkins-' }
    tools {
        jdk 'Java17'
        maven 'Maven3'
    }
}
    stages{
        stage("Cleanup Workspace"){
                steps {
                cleanWs()
                }
        }

        stage("Checkout from SCM"){
                steps {
                    git branch: 'main', credentialsId: 'github', url: 'https://github.com/poojayou/register-app.git'
                }
        }

        stage("Build Application"){
            steps {
                sh "mvn clean package"
              }

        }
 }
