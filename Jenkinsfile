pipeline {
    agent any

    environment {
        DOTNET_CLI_TELEMETRY_OPTOUT = '1'
        BUILD_CONFIGURATION = 'Release'
    }

    stages {
        stage('Restore') {

            steps {
                bat 'dotnet restore'
            }
        }

        stage('Build') {            

            steps {
                bat 'dotnet build --no-restore'
            }
        }

        stage('Test') {

            steps {
                bat 'dotnet test--no-build --verbosity normal'
            }
        }
    }
}