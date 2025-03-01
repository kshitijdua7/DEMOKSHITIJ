pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/kshitijdua7/DEMOKSHITIJ.git'
            }
        }
        
        stage('Build') {
            steps {
                script {
                    def javaFileExists = fileExists('Main.java')
                    if (javaFileExists) {
                        sh 'javac Main.java'
                        echo "Build Successful"
                    } else {
                        echo "No Main.java found, skipping build"
                    }
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    def classFileExists = fileExists('Main.class')
                    if (classFileExists) {
                        sh 'java Main'
                        echo "Tests Passed"
                    } else {
                        echo "No compiled Main class found, skipping test"
                    }
                }
            }
        }
    }
}
