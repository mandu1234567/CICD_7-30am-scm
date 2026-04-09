pipeline {
    agent any

    stages {
        stage('git checkout') {
            steps {
               git branch: 'main', url: 'https://github.com/mandu1234567/MANDU-terraform-7-30am.git'
            }
        }
         stage('init') {
            steps {
                dir('terraform-day-1') {
                  sh  'terraform init'
              
                }
            }
        }
        stage('plan') {
            steps {
               dir('terraform-day-1') {
                  sh  'terraform plan'
              
                }
            }
        }
        stage('apply') {
            steps {
                dir('terraform-day-1') {
                  sh  'terraform apply -auto-approve'
              
                }
            }
        }
      
    }
}
