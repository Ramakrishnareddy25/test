pipeline {
    agent any

    stages {
        stage('Generate File') {
            steps {
                // Your script to generate the file
                  sh 'echo "Hello, world!" > myfile.txt'
            }
        }

        stage('Store File in GitHub') {
            steps {
                // Clone the public repository
                git branch: 'master', url: 'https://github.com/Ramakrishnareddy25/test.git'

                // Copy generated file to the repository
                sh 'cp myfile.txt .'

                // Add, commit, and push changes
                git add '.'
                git commit message: 'Generated file from Jenkins pipeline'
                git push origin master
            }
        }
    }
}
