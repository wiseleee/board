def mainDir="."
def ecrLoginHelper="docker-credential-ecr-login"
def region="ap-northeast-1"
def ecrUrl="598552988151.dkr.ecr.ap-northeast-1.amazonaws.com"
def repository="board"
def deployHost="54.168.148.170"

pipeline {
    agent any

    stages {
        stage('Pull Codes from Github'){
            steps{
                checkout scm
            }
        }
        stage('Build Codes by Gradle') {
            steps {
                sh """
                cd ${mainDir}
                ./gradlew clean build
                """
            }
        }

    }
}
