pipeline{
    agent any

    stages{
        stage('Code Checkout'){
            steps{
                echo "Checking out code from git repository"
                checkout scm

            }            
        }
        stage('Run Python Script'){
            steps{
                echo "Running the Python script from the git repository"
                sh 'python3 numbers.py'
            }
        }
    }
    post {
        always {
            echo 'Pipeline execution completed.'
        }
    }
}