pipeline {
    agent any
    environment{
        PATH = "/opt/maven/apache-maven-3.8.2/bin/:$PATH"
    }
    stages {
        stage("clone code") {
            steps {
              git credentialsId: 'git_credentials', url: 'https://github.com/rahul3851/hello-world.git'
            }
        }
        stage("build code") {
            steps {
              sh "mvn clean install"
            }
        }
    }
