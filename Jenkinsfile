node {
    def app

    stage('Clone repository'){
        checkout scm
    }

    stage('Build image'){
        app = docker.build("javatest/test")
    }

    stage('Test Image'){

        sh 'echo "Image Created"'
    }


}