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
                junit '**/target/surefire-reports/*.xml' // 收集单元测试报告的调用过程
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
