pipeline {
    agent { 
        environment{
            PATH = "C://WINDOWS//System32"
        }
        node {
            label 'Sanket_pc'
            }
      }
    triggers {
        pollSCM '* * * * *'
    }
     stages {
        stage('Build') {
            steps {
                echo "Building.."
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                bat '''
                python hello.py
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo "Delivery.."
            }
        }
    }
}
