pipeline {
    agent any
    stages {
        // stage('Clone repository') {
        //     steps {
        //         checkout([$class: 'GitSCM', 
        //             branches: [[name: '*/main']], 
        //             userRemoteConfigs: [[url: 'https://github.com/SanketMuttur/PES1UG23CS846_Jenkins.git']]
        //         ])
        //     }
        // }
        stge('Build') { //#IntentionalError - stge != stage
            steps {
                build 'PES1UG23CS846-1'
                sh 'g++ main.cpp -o output'
                sh '#IntentionalErrorXD'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
