pipeline {
    agent any

    stages {
        stage('SCM Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Compile-Package') {
            steps {
                script {
                    def mvnHome = tool name: 'maven-3', type: 'maven'
                    if (isUnix()) {
                        sh "${mvnHome}/bin/mvn -B clean package"
                    } else {
                        bat "\"${mvnHome}\\bin\\mvn.cmd\" -B clean package"
                    }
                }
            }
        }
    }
}
