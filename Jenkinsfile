pipeline {
    agent any

    tools {nodejs('Node')
          }

    stages {

        stage('Install dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build application') {
            steps {
            	sh 'npm start '
            }
        }

        stage('Run Functional Tests') {
            steps {
              sh 'npm run test.e2e.sauce.eu ${env.CLI_ARGS}'
            }
        }
    }
}
