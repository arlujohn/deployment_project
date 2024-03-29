pipeline {
    agent any
    //environment{}
    parameters{
        choice(choices: ['YES','NO'],description:'Start the web app?',name:'START')
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh "ls -lhrt"
                dir('MySampleWebsite'){
                    sh "ls -lhrt"
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}