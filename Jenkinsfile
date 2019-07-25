pipeline {
    agent any
    triggers {
        cron('H/1 * * * *')
    }
    stages {
       
        stage('Build') {
            steps {
        
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
                sh 'mvn package -Dmaven.test.skip=true'
                echo "Building is done."
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
                echo "Junit test finished."
            }
        }
    }
}
