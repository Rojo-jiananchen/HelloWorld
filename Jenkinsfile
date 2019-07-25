pipeline {
    agent any
    def triggers = [] 
    if (env.BRANCH_NAME != 'master') {
      triggers << [
        $class: 'hudson.triggers.TimerTrigger',
        spec: "H/3 * * * *" 
      ]
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
