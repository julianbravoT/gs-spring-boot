pipeline {
    agent {
        label 'slave-1'
    }
    
    tools {
        maven 'maven3'
    }

    stages {
        stage('git chechout') {
            steps {
                git branch: 'develop', url: 'https://github.com/Zillaphresh/gs-spring-boot.git'
            }
        }
        stage('build') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
