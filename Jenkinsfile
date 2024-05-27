pipline {
    agent { label 'Jenkins-Agent' }
    tools {
        jdk 'Java17'
        maven 'Maven3'
    }

    stages {
        stage("Cleanup Workspace") {
            steps {
                cleanWs()
            }
                }
        stage("Checkin to github") {
            steps{
                 git branch: 'main', credentialsId: 'github', url: 'https://github.com/MohamedAboali/register-app'
                }
            }
        stage("Build the application"){
            steps {
                sh "mvn clean package"
            }
        }
        stage("Test the application"){
            steps {
                sh "mv test"
            }
        }

    }   

}