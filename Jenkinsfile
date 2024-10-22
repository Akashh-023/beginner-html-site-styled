pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the gh-pages branch
                git branch: 'gh-pages', url:  'https://github.com/Akashh-023/beginner-html-site-styled.git'
            }
        }
        stage('Pull Code') {
            steps {
                // Create a directory and copy the code (adjusted for Linux environment)
                script {
                    sh 'mkdir -p ~/Documents/code'  // '-p' ensures the parent directories are created
                    sh 'cp -r * ~/Documents/code'  // '-r' for recursive copy
                }
            }
        }
    }
}
