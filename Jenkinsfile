pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES1UG21CS058-1'
                sh 'g++ main.cpp -o output'
                
            }
        }
        stage('Test') {
            steps {
                shh './output'
                
            }

        }
        stage('Deploy') {
            steps {
                sh './non_existing_script.sh'
               
                echo 'Deploy'
                '
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
