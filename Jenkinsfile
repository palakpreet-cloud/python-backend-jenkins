pipeline{
    agent any
    stages{
        stage('git'){
            steps{
                git url: 'https://github.com/palakpreet-cloud/python-backend-jenkins.git', branch: 'main', , credentialsId: 'pythonbackendjenkinsfile'
            }
        }
        stage('venv'){
            steps{
                sh 'python3 -m venv venv'
            }
        }
        stage('install'){
            steps{
                sh 'venv/bin/pip install -r requirements.txt'
            }
        }
        stage('start'){
            steps{
                sh 'venv/bin/python3 unified_main.py'
            }
        }

    }
}
