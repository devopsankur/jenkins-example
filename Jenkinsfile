pipeline {
    agent any
    stages {
        stage ('SCM Checkout') {

            steps {
                   git url: 'https://github.com/devopsankur/jenkins-example.git',branch: 'master'
                }
            }
        }
    stages {
        stage ('Compile Stage') {

            steps {
                def mavenHome =  tool name: "maven-3", type: "maven"
                def mavenCMD = "${mavenHome}/bin/mvn"
                sh "${mavenCMD} clean compile"
            }
        }

        stage ('Testing Stage') {

            steps {
                def mavenHome =  tool name: "maven-3", type: "maven"
                def mavenCMD = "${mavenHome}/bin/mvn"
                sh "${mavenCMD} test"
            }
        }


        
    }
}
