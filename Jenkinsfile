pipeline {
    agent any
    options{
        timeout(time: 10, unit: "SECONDS")
        disableConcurrentBuilds()
    }
    
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
        stages {
            stage("build") {
                steps {
                   
                    sh " echo this is build "
                    
                }
            }
              stage("Test") {
                steps {
                 
                    sh "echo this is test"
    
                   
                }
            }
              stage("deploy") {
                steps {
                   
                    sh "echo this is deploy"
                    
                }
            }
            stage('Example') {
            steps {
                echo "Hello ${params.PERSON}"
                echo "Biography: ${params.BIOGRAPHY}"
                echo "Toggle: ${params.TOGGLE}"
                echo "Choice: ${params.CHOICE}"
                echo "Password: ${params.PASSWORD}"
            }
        }
        }

        post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure {
            echo ' i will be failure'
        }
        success {
            echo 'It will be success'
        }
    }
    
}
