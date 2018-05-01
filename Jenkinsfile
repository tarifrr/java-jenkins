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
            sh 'java Hello'
        }

    }


}