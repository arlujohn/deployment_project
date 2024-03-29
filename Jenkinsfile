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
            when{
                parameters.START == 'YES'
            }
            steps {
                echo 'Testing..'
                echo 'Running the Web App'
                dir('MySampleWebsite'){
                    sh "python3 manage.py runserver"
                }
            }
        }
    }
}