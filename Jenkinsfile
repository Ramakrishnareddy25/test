pipeline {
    agent any

    stages {
        stage('Generate File') {
            steps {
                // Your script to generate the file
                  sh 'echo "Hello, world!" > myfile1.txt'
            }
        }

        stage('Store File in GitHub') {
            steps {
                // Clone the public repository
                git branch: 'master', url: 'https://github.com/Ramakrishnareddy25/test.git'
                sh 'cd test'
                // Copy generated file to the repository
                sh 'ls -l'
                sh 'cp -r myfile1.txt .'

                // Add, commit, and push changes
                sh 'git add .'
                sh 'git commit -m first'
                sh 'git push origin master'
            }
        }
    }
}
