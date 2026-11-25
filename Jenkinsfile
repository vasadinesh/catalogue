// @Library('jenkins-shared-library') _

// def configMap = [
//     project: "roboshop",
//     component: "catalogue"
// ]
// if (env.BRANCH_NAME.equalsIgnoreCase('main')){
//     nodejsEKSMain(configMap)
// }
// else {
//     nodejsEKSPipeline(configMap)
// }


pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building Catalogue application'
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
    }
}
