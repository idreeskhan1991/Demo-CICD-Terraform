pipeline {
    agent any
    
    tools {
        terraform 'terraform'
    }
    stages {
        stage ("checkout from GIT") {
            steps {
                git branch: 'main', credentialsId: 'aa3e80aa-e369-421e-a28e-21c892e2e6da', url: 'https://github.com/idreeskhan1991/Demo-CICD-Terraform.git'
            }
        }
        stage ("terraform init") {
            steps {
                bat 'terraform init'
            }
        }
        stage ("terraform fmt") {
            steps {
                bat 'terraform fmt'
            }
        }
        stage ("terraform validate") {
            steps {
                bat 'terraform validate'
            }
        }
        stage ("terrafrom plan") {
            steps {
                bat 'terraform plan '
            }
        }
        stage ("terraform apply") {
            steps {
                bat 'terraform apply --auto-approve'
            }
        }
        stage ("terraform destroy") {
            steps {
                bat 'terraform destroy --auto-approve'
            }
        }
    }
}
