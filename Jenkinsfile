node {
    def app

    stage('Clone repository') {
        
        checkout scm
    }

    stage('Build image') {

        app = docker.image('python:3.6.6')
    }

    stage('Test image') {

        app.inside {
            sh 'python3.6 hello_world.py'
        }
    }
}
