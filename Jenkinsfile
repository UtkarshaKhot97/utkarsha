pipeline {
    agent { node { label 'built-in' } }
    parameters {
                    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    }
    stages {
        stage('SCM checkout') {
            steps {
                sh 'rm -rf game-of-life'
                sh 'git clone https://github.com/UtkarshaKhot97/game-of-life.git'
                 echo 'SCM checkout successfull'
            }
        }
        stage('Build') {
            steps {
                sh 'pwd'
                echo 'Build Successfully'
            }
        }
        stage ('Test'){
            steps {
                sh 'mvn -version'
                echo 'Test successfull'
            }
        }
        stage('Deploy') {
            steps {
                sh 'mvn -version'
                sh 'cd .'
                echo 'Build Successfully'
            }
        }
    }
}


