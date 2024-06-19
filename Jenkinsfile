pipeline {
    agent
    {
    label 'AGENT-1'
    }
    options {
         timeout(time: 30, unit: 'MINUTES')
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
        stage('Build') {
            steps {
                sh 'echo build'
            }
        }
        stage('Test') {
            steps {
               sh 'echo test'
               sh 'sleep 10'
            }
        }
        stage('Deploy') {
            steps {
               sh 'echo deploy'
            }
        }
         stage('Example') {
            steps {
               echo "Hello ${params.PERSON}"
               echo "Biography: ${params.BIOGRAPHY}"
               echo "Toggle: ${params.TOGGLE}"
               echo "Choice: ${params.CHOICE}"
               echo "trigger test"
               echo "trigger test1"
               echo "trigger test2"
               echo "trigger again"
               }
         }
    }
}