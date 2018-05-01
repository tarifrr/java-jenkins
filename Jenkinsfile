node {
    def app

    stage('Clone repository'){
        checkout scm
    }

    stage('Build image'){
        app = docker.build("javatest")
    }

    stage('Run Image'){
        docker.image('javatest:latest').inside {
            sh 'pwd'
            sh 'javac Hello.java'
            sh 'java Hello'
        }
    stage('See Docker Images'){
        sh 'docker images'
    }

    }


}