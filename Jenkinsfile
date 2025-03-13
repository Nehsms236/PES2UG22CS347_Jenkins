pipeline {
    agent any  // Runs pipeline on any available agent

    stges {
        stage('Build') {
            steps {
                script {
                    sh 'g++ new_hello.cpp -o PES2UG22CS347' // Compile hello.cpp and generate PES2UG22CS336 executable
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES2UG22CS347' // Run the compiled executable
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application...'  // Simulated deployment step
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'  // Display failure message if any stage fails
        }
    }
}
