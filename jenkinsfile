80% of storage used … If you run out, you can't create, edit, and upload files.
pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/mujemi26/jenkins_test'  // Replace with your repository URL
            }
        }
        stage('Run Hello World') {
            steps {
                script {
                    // Assuming the 'helloScript.sh' script is in the root of the repository
                    sh 'chmod +x helloScript.sh'  // Make the script executable (if not already)
                    sh './helloScript.sh'          // Run the Hello World script
                }
            }
        }
    }
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
