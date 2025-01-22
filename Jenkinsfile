pipeline {
    agent any

    stages {
        stage('clone') {
            steps {
              git branch: 'main', url: 'https://github.com/lumlathomas/Terraform-CICD.git'
            }
        }
        stage('init') {
            steps {
                sh 'terraform init'
            }
        }
         stage('plan') {
            steps {
                sh 'terraform plan'
            }
        }
    }
}

// example 1.	Working with scripted pipeline

// node {
//     stage('stage-1') {
//         sh 'touch stage-1'
//     }
//     stage('stage-2') {
//         sh 'touch stage2'
//     }
//     stage('stage3') {
//         sh 'touch stage3'
//     }
// }

// example 2.	Working with staged or declarative pipelines


// pipeline {
//     agent any
 
//     stages {
//         stage('git clone') {
//             steps {
//                 git branch: 'main', url: 'https://github.com/lumlathomas/TerraformClass.git'
//             }
//         }
//         stage('terraform init') {
//             steps {
//                 dir('Day-1-Terraform-Basics'){
//                 sh 'terraform init'
//                 }
//             }
//         }
//         stage('terraform plan') {
//             steps {
//                 dir('Day-1-Terraform-Basics'){
//                 sh 'terraform plan'
//                 }
//             }
//         }
//         // stage('terraform apply') {
//         //     steps {
//         //         sh 'terraform apply -auto-approve'
//         //     }
//         // }
//     }
// }
