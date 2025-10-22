pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application'
                g++ main.cpp -o main.out
            }
        }
        stage('Test') {
            steps {
                echo 'Testing the application'
                chmod +x main.out
                ./main.out
            }
        }

    }
}
