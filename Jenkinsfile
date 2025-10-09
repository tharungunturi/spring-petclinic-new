pipeline {
    agent any

    stages{
        stage('git clone') {
            steps {
                git branch: '2.1-master', credentialsId: 'tharun', url: 'https://github.com/tharungunturi/thymeleafexamples-petclinic.git'
            }
        }

        stage('list'){
            steps{
                sh 'ls -l'
            }
        }
        stage('validate'){
            steps{
                sh 'mvn validate'
            }
    }

     stage('clean'){
            steps{
                sh 'mvn clean'
            }
    }

    stage('compile'){
            steps{
                sh 'mvn compile'
            }
    }

    stage('package'){
            steps{
                sh 'mvn package'
            }
    }
}
}
