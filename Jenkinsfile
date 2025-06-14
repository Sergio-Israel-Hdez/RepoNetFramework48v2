pipeline {
    agent any

    environment {
        SOLUTION = 'RepoNetFramework48v2.sln'  // Reemplaza con el nombre real de tu .sln
        BUILD_CONFIGURATION = 'Release'
        OUTPUT_DIR = 'output'
    }

    tools {
        msbuild 'MSBuild_16' // Configúralo en Global Tool Configuration
    }

    stages {
        stage('Checkout') {
            steps {
                bat 'git checkout master'
                bat 'git pull origin master'
            }
        }

        stage('Restore Packages') {
            steps {
                bat 'nuget restore'
            }
        }

        stage('Build') {
            steps {
                bat 'msbuild'
            }
        }
    }

    post {
        failure {
            echo '❌ La build falló.'
        }
        success {
            echo '✅ Build finalizada con éxito.'
        }
    }
}