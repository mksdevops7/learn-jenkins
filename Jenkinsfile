﻿pipeline {
    agent any {
       node { label 'workstation'}
    }

    environment {
       SAMPLE_URL = "https://sample.com"
       SSH = credentials("ssh")
    }

    options {
       ansiColor('xterm')
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
               sh 'echo Build'
               sh 'echo $SAMPLE_URL'
               sh 'echo $SSH'
                //
            }
        }
        stage('Test') {
            steps {
               sh 'echo Test'
                //
            }
        }
        stage('Deploy') {
            steps {
               sh 'echo Deploy'
                //
            }
        }
    }
}