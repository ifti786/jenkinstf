pipeline {
    agent any
        stages {
        stage('Terraform Started') { 
            steps {
                sh 'echo "Started....."'
            }
        }
        stage('Terraform Init') { 
            steps {
                sh "/terraform/terraform init" 
            }
        }
        stage('Terraform plan') { 
            steps {
                sh "/terraform/terraform plan"
            }
        }
stage('Terraform ended')
	steps {
	sh 'echo "Terraform deployment end"'
    }
}

