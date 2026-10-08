pipeline {
    agent any

    stages {

        stage('Pull Git Content') {
            steps {
                dir('git-content') {
                    git branch: 'develop',
                        url: 'https://github.com/bhargavmahajan17/jenkins-demo.git'
                }
            }
        }

        stage('Verify Content') {
            steps {
                sh 'echo "Git content pulled successfully!"'
                sh 'ls -la git-content'
                sh 'cat git-content/index.html'
            }
        }
    }
}
