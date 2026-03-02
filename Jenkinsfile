pipeline {
    agent any

    stages {
        stage('Fetching File..') {
            steps {
               git branch: 'master', url : "https://github.com/Aditya-Suresh25/jenkins-demo.git"
            }
        }
        stage('Build') {
            steps {
                echo 'Building Project....'
                bat "javac Hello.java"
            }
        }
        stage('Executing..') {
            steps {
                echo 'Executing Program'
                bat "java Hello"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Project..'
            }
        }
    }
    post{
        success{
            echo "Pipeline executed successfully!"
        }
        failure{
             echo "Pipeline failed"
        }
    }
}
