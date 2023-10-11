pipeline { 
    agent {
    node {
        label 'built-in'
        customWorkspace '/home/ec2-user'
    }
}
    
     
    
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
                sh '''
                touch utkarsha.txt
                pwd
                '''
                echo 'Build Successfully'
            }
        }
        stage ('Test'){
            steps {
                echo 'for build numbers /$ { BUILD_NUMBERS} -> ${BUILD_NUMBERS}'
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


