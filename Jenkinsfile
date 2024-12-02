pipeline {
    agent { label "builder1"}
    tools{
        maven "maven3.9.9"
    }
    stages {
        stage('stage1--preparing for build') {
            steps {
                echo 'preparing..'
            }
        }
         stage('stage2--clone the project') {
            steps {
                git branch: 'main', credentialsId: 'e1a6f3f5-f3dd-4ed8-93c3-92f87dc60b74', url: 'https://github.com/Kalpakkarmore/devops-pipelines.git'
            }
        }
         stage('stage3--build the project') {
            steps {
                sh "pwd"
                sh "ls"
                sh "/opt/maven/bin/mvn install"
            }
        }
         stage('stage5--copy the artefact to artefactory') {
            steps {
                echo 'copying artefacts'
            }
        }
    }
}
