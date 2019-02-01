#!groovy
node{
    stage('check out the code'){
        git branch: 'development', credentialsId: 'ba8eea67-50ea-49a8-88c2-3b161b088f52', url: 'https://github.com/kumarbasha/maven-web-application.git'
    }
    stage('Build'){
        if(isUnix()){
            def mavenhome = tool name: 'M2_HOME', type: 'maven'
            sh "${mavenhome}/bin/mvn test"
        }
        else{
            bat 'mvn test'
        }
    }
}
