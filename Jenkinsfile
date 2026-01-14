pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Building on branch ${env.BRANCH_NAME}"
            }
        }

        stage('Build Dev-2') {
            when {
                branch 'dev-2'     // only deploy on main
            }
            steps {
                echo "Building on branch ${env.BRANCH_NAME}"
            }
        }

        stage('Test') {
            steps {
                echo "Testing on branch ${env.BRANCH_NAME}"
            }
        }

        stage('Deploy') {
            when {
                branch 'main'     // only deploy on main
            }
            steps {
                echo "Deploying from ${env.BRANCH_NAME}"
            }
        }
    }
}
