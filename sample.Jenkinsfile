pipeline {
    agent any
    environment { 
        url = "global.com"
        SSH_CREDS = credentials('SSH_CREDS')
    }

    options {
        timeout(time: 1, unit: 'MINUTES')
        buildDiscarder(logRotator(numToKeepStr: '1'))
        disableConcurrentBuilds(abortPrevious: true)
         
    }

    stages {
        stage('Stage one') {
            steps {
                echo "url is ${url}"
            }
        }

        stage('Stage Two') {
            environment { 
                url = "local.com"
            }
            steps {
                echo "Url is ${url}"
            }
        }

        stage('Stage Five') {
            steps {
                sh '''
                echo "Hey Hi Amrutha!"
                echo "Muskoni kurcho"
                env
                '''
            }
        }
    }

}