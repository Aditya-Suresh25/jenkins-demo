pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Quotes added to branch and url strings
                git branch: 'master', url: 'https://github.com/Aditya-Suresh25/jenkins-demo.git'
            }
        }
        stage('Publishing') {
            steps {
                // Added target: key and fixed string quoting/capitalization
                publishHTML(target: [
                    allowMissing: true,
                    alwaysLinkToLastBuild: false,
                    keepAll: false,
                    reportDir: '.',
                    reportFiles: 'index.html',
                    reportName: 'Sample Html Page Jenkins'
                ])
            }
        }
    }
}
