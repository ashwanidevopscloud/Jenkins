pipeline {
    agent any 
        stages {
            stage("build") {
                steps {
                    script{
                        sh "this is build"
                    }
                }
            }
              stage("Test") {
                steps {
                    script{
                        sh "this is test"
                    }
                }
            }
              stage("deploy") {
                steps {
                    script{
                        sh "this is deploy"
                    }
                }
            }
        }
    
}