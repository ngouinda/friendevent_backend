pipeline {
    agent {
        node {
            label 'agent_composer'
        }
    }

    stages {
        stage('CI') {
            steps {
                git branch: 'main', url: 'https://github.com/fredericBui/friendevent_backend.git'
                sh 'composer install'
                sh 'php bin/phpunit'
            }
        }
    }
}
