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
                 C:\Users\HP\AppData\Local\Programs\Python\Python312  hello.py
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
