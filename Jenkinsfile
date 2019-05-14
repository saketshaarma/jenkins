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
            echo 'This will run only if successful'
        }
        failure {
            mailext body: 'A Test EMail', recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']], subject: 'Test'
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
