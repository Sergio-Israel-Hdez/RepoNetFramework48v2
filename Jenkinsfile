
node {
    stage('Checkout') {
        // Checkout the source code from the repository
        checkout scm
    }

    stage('Restore NuGet Packages') {
        // Restore NuGet packages
        bat 'nuget restore'
    }

    stage('Build') {
        // Build the .NET Framework 4.8 project
        bat 'msbuild /p:Configuration=Release /p:Platform="Any CPU"'
    }
}