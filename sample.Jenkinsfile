pipeline {
    agent any
    environment { 
        url = "global.com"
        SSH_CREDS = credentials('SSH_CREDS')
    }

    options {
        // timeout(time: 26, unit: 'SECONDS')
        // buildDiscarder(logRotator(numToKeepStr: '1'))
        // disableConcurrentBuilds(abortPrevious: true)

    }

    tools {
        maven 'mvn-396'
    }

    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    stages {
        stage('Stage one') {
            steps {
                echo "url is ${url}"
                sleep(1)
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