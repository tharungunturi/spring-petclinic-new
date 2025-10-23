pipeline {
    agent any

    stages{
        stage('git clone') {
            steps {
                git branch: 'main', credentialsId: 'tharun', url: 'https://github.com/tharungunturi/spring-petclinic-new.git'
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
    stage('deploy'){
            steps{
                sh 'mvn deploy'
            }
    }
}
}
