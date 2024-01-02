pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/fajri-isnanto/tlab'
            }
        }
        stage('Build Image'){
            steps {
                sh '''
                        #!/bin/bash
                        docker build -t web-app /var/lib/jenkins/workspace/TLAB/web-vote-app .   
                        # Add more commands as needed
                    '''
            }
            // steps {
            // sh  docker build -t worker-app /var/lib/jenkins/workspace/TLAB/vote-worker .   
            // }
            // steps {
            // sh  docker build -t results-app /var/lib/jenkins/workspace/TLAB/results-app .   
            // }
        }
    }
}
