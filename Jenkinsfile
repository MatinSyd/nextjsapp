pipeline {
    agent any

    stages {
        stage('Install Dependencies') {
            steps {
                script {
                    // Use NodeJS from the tool configuration
                    def nodejs = tool 'Node.js'
                    env.PATH = "${nodejs}/bin:${env.PATH}"

                    // Install dependencies
                    sh 'npm install'
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    // Build the Next.js app
                    sh 'npm run build'
                }
            }
        }
    }
}
