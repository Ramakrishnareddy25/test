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
                // Copy generated file to the repository
                sh 'ls -l'
                // sh 'cp -r myfile1.txt .'

                // Add, commit, and push changes
                sh 'git config --global user.email "ramakrishnareddytetali@gmail.com"'
                sh 'git config --global user.name "ramakrishnareddy25"'
                sh 'git add .'
                sh 'git commit -m first'
                sh 'git push https://github.com/Ramakrishnareddy25/test.git master'
            }
        }
    }
}
