pipeline {
    stage('SCM Checkout') {
        git 'https://github.com/azizjon-nigmatjonov/java-example'
    }
    stage('Compile-Package') {
        def mvnHome = tool name: 'maven-3', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
}
