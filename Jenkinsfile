pipeline {
    agent any
    stages {
        stage('---clean---'){
            steps {
                echo "Hello India"
            }
        }
        stage('---Build---'){
          steps {
              echo "It is my country"
          }
        }
        stage('---deployment---'){
          steps {
            echo "I love my country"
          }
        }
        stage('---Completion---'){
          steps {
            echo "I love its people"
          }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            mail bcc: '', body: "<b>Example</b><br>Project: ${env.JOB_NAME} <br>Build Number: ${env.BUILD_NUMBER} <br> URL de build: ${env.BUILD_URL}", cc: '', charset: 'UTF-8', from: '', mimeType: 'text/html', replyTo: '', subject: "ERROR CI: Project name -> ${env.JOB_NAME}", to: "saketbsharma@gmail.com";
        }
        failure {
           mail bcc: '', body: "<b>Example</b><br>Project: ${env.JOB_NAME} <br>Build Number: ${env.BUILD_NUMBER} <br> URL de build: ${env.BUILD_URL}", cc: '', charset: 'UTF-8', from: '', mimeType: 'text/html', replyTo: '', subject: "ERROR CI: Project name -> ${env.JOB_NAME}", to: "saketbsharma@gmail.com";
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}
