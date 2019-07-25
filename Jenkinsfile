pipeline {
    agent any
    
    triggers {
        cron('H 4/* 0 0 1-5')
    }
    
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
    }
}
