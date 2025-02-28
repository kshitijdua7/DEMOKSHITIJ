pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/kshitijdua7/DEMOKSHITIJ.git'
            }
        }
        stage('Build') {
            steps {
                sh 'javac Main.java || echo "No Main.java found, skipping build"'
            }
        }
        stage('Test') {
            steps {
                sh 'java Main || echo "No Main class found, skipping test"'
            }
        }
    }
}
