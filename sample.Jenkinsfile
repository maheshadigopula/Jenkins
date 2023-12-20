pipeline {
    agent any
    environment { 
        url = "global.com"
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
                echo "Hello Amrutha"
            }
        }
    }

}