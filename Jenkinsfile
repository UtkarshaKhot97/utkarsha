pipeline {
    agent { node { label 'built-in' } }
    parameters {
                    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    }
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Build') {
            steps {
                sh 'java -version'
                echo 'Build Successfully'
            }
        }
        stage('Test'){
            steps {
                sh 'mvn -version'
                echo 'test successfull'
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
