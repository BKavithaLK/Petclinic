pipeline {
    agent any
    
    tools{
        maven 'Maven3'
    }

    stages {
        stage('git checkout') {
            steps {
               git branch: 'main', url: 'https://github.com/BKavithaLK/Petclinic.git'
            }
        }
        stage('Maven compile'){
            steps{
                sh 'mvn clean compile'
            }
        }
        stage('Maven Build'){
            steps{
                sh 'mvn clean package -DskipTests=true'
            }
        }
    }
}
