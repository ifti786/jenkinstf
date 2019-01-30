pipeline {
    agent {
	node {
		label 'master'
	  }
	}
        stages {

        stage('Terraform Started') { 
            steps {
                sh 'echo "Started....."'
            }
        }
	stage('git clone') {
	steps {
		sh 'rm -rf *'
		sh 'git clone https://github.com/ifti786/jenkinstf.git'
		}
	 }
        stage('Terraform Init') { 
            steps {
                sh "/terraform/terraform init ./jenkinstf" 
            }
        }
        stage('Terraform plan') { 
            steps {
                sh "/terraform/terraform plan ./jenkinstf"
            }
        }
stage('Terraform ended') {
	steps {
	sh 'echo "Terraform deployment end"'
    }
}
}
}
