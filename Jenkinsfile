pipeline{
    agent any
    stages{
        stage("Git"){
            steps{
                git url:"https://github.com/MartiMarch/formacion-jenkins-groovy.git"
            }
        }
        stage("Maven"){
            steps{
                script{
                    sh "chdir=${WORKSPACE}/NetworkScanner mvn validate compile test package verify install"
                }
            }
        }
    }
}