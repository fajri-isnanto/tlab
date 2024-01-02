pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/fajri-isnanto/tlab'
            }
        }
        
        stage('Build Image'){
            agent {
            docker { image 'ubuntu' }
            steps {
            docker build -t web-app ./web-vote-app .   
            }
            }
        }
    }
}
