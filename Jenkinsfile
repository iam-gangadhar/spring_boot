@Library('my-shared-lib') _
pipeline{
    agent any

    stages{
        stage('Git Checkout'){
            steps{
                gitCheckout(
                    branch: "main",
                    url: "https://github.com/gangadhar-aws/spring_boot.git"
                )
            }
        }

        stage('Maven Unit Test'){
            steps{
               mvnTest()
            }
        }

        stage('Integration Test Maven'){
            steps{
               mavenIntegration()
            }
        }




    }
}