pipeline {
    agent {
        label 'centos'
    }
    stages {
        stage('Get from GItHub repository') {
            steps {
                git branch: 'main', credentialsId: 'e4fe6732-267d-46b9-b7ff-3c6cc43a8cb4', url: 'git@github.com:Sergej1024/Vector-role.git'
            }
         }
        stage('Install requirements') {
            steps {
                sh 'pip install -r tox-requirements.txt'
            }
        }
        stage('Run molecule test') {
            steps {
                sh 'molecule test'
            }
        }
        stage('Delete workspace') {
            steps {
              cleanWs()
            }
        }
    }
}