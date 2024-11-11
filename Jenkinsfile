
pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
              git branch: 'main' , url:  'https://github.com/mujemi26/jenkins_test.git'  // Replace with your repository URL
            }
        }
        stage('Run Hello World') {
            steps {
                script {
                    
                    sh 'chmod +x helloScript.sh'  // Make the script executable (if not already)
                    sh './helloScript.sh' 
                    '''
                    // Run the Hello World script
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
