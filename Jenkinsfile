pipeline{
    agent any
    tools {
  terraform 'Terraform'
}
stages{
    stage('git checkout'){
        steps{
            git 'https://github.com/galamsiva2020/Project_Terraform.git'
           // git credentialsId: 'GitHub', url: 'https://github.com/galamsiva2020/Project_Terraform.git'
        }
    }
    stage('Terraform initalization'){
        steps{
            sh 'terraform init'
        }
    }
    stage('Terraform showing plan'){
         steps{
             sh 'terraform plan'
         }
    }
    stage('Provisioning Resources'){
         steps{
             sh 'terraform apply --auto-approve'
              //sh 'terraform destroy --auto-approve'
         }
    }
}
}
