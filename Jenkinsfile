pipeline {
    agent any
    stages {
	stage('Git-Checkout') {
        steps {
                echo 'Checking out from Git Repo';
                git 'https://github.com/simplilearn-github/Pipeline_Script.git';
            }
        }
        stage('Build') {
            steps {
                echo 'Building the check out project';
                bat 'Build.bat';
            }
        }
        stage('Unit-Test') {
            steps {
                echo 'Running JUnit Test';
                bat 'Test.bat';
            }
        }
        stage('Quality-Gate') {
            steps {
                echo 'Verifying Quality Gates';
                bat 'Quality.bat';
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying to stage environment for more tests!';
                bat 'Deploy.bat';
            }
        }
    }
} 
