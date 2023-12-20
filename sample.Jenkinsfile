pipeline {
    agent any
    environment { 
        url = "global.com"
        SSH_CREDS = credentials('SSH_CREDS')
    }

    options {
        timeout(time: 26, unit: 'SECONDS')
        buildDiscarder(logRotator(numToKeepStr: '1'))
        disableConcurrentBuilds(abortPrevious: true)

    }

    stages {
        stage('Stage one') {
            steps {
                echo "url is ${url}"
                sleep(30)
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