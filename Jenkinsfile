pipeline {
    agent any

    environment {
        // Define any additional environment variables needed for the pipeline
        NODE_VERSION = '16.x'
        NPM_REGISTRY = 'https://registry.npmjs.org/'
    }

    stages {
        stage('Install Dependencies') {
            steps {
                // Use Node.js and npm from the Global Tool Configuration
                tools {
                    nodejs "${env.NODE_VERSION}"
                }
                // Install Node.js dependencies using npm
                sh "npm install --registry=${env.NPM_REGISTRY}"
            }
        }

        // Other stages of your pipeline...
    }

    // Post-build actions and notifications...
}
