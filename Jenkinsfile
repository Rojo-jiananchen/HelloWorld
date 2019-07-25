pipeline {
    agent any
    triggers {
        cron('H/1 * * * *')
    }
    stages {
        stage('Test') {
            steps {
                sh 'mvn test'
                echo "Junit test finished."
            }
        }
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
