pipeline {
    agent { 
        node {
            label 'Sanket_pc'
            }
      }
     environment{
            PATH = "C://WINDOWS//System32"
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
