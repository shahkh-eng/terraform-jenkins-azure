pipeline {
    agent any
    
    tools {
        terraform 'terraform'
    }
    stages {
        stage ("checkout from GIT") {
            steps {
                git 'https://github.com/shahkh-eng/terraform-jenkins'
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
    }
}
