pipeline{
    agent any
    
    triggers {
        pollSCM('* * * * *')
    }
    
    stages{
        stage('Repository Location'){
            steps{
                echo 'Connecting to the git repository...'
                git branch: 'main', url: 'https://github.com/DCI-xurxo/git-jenkins.git'
            }
        }

        stage('Run Python Script'){
            steps{
                echo 'Running the Python script...'
                sh 'python3 test.py'
            }
        }
    }

    post{
        always{
            echo 'Pipeline execution completed.'
        }
    }
}

tables()
print("Hello")
print("this is aws jenkins")