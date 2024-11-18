pipeline{
    agent {
        docker {
            image  'python:3.8-slim'
            args '-u root:root' 
        }
    }
    stages{
        stage('chekout'){
            steps{
                git url : 'https://github.com/ShijithDG/docker-practise-nov.git'
            }
        }
        stage('install dependencies'){
            steps{
                sh 'pip install -r requirement.txt'
            }
        }
        stage('package'){
            steps{
                sh 'tar -cvf  my_app.tar.gz app.py'
                echo'successfuly completed making zip file'
            }
        }
    }
}