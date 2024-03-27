pipeline{
    agent {
        label 'agent-linux'
    }
    tools {
        terraform 'terraform-11'
    }
    
    stages{
        stage('Git Checkout'){
            steps{
                git 'https://github.com/mshan011181/terraform-shan-project.git'
            }
        }
        stage('Get Directory') {
            steps{
                println(WORKSPACE)
            }
        }
        stage('Terraform init'){
            steps{
                sh 'terraform init'
             }
        }
        stage('Terraform Destroy'){
            steps{
                sh 'terraform destroy --auto-approve'
                   }
          }
     }
  }
 
