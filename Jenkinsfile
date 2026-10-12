
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Restore') {
            steps {
                bat 'dotnet restore SeleniumBasicExercise.sln'
            }
        }

        stage('Test Project 1') {
            steps {
                bat 'dotnet test TestProject1/TestProject1.csproj --configuration Release'
            }
        }

        stage('Test Project 2') {
            steps {
                bat 'dotnet test TestProject2/TestProject2.csproj --configuration Release'
            }
        }

        stage('Test Project 3') {
            steps {
                bat 'dotnet test TestProject3/TestProject3.csproj --configuration Release'
            }
        }
    }
}
