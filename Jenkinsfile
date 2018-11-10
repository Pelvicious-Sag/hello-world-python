node {
    def app

    stage('Clone repository') {
        
        checkout scm
    }

    stage('Build image') {

        app = docker.image('python')
    }

    stage('Test image') {

        app.inside {
            sh 'python hello_world.rb'
        }
    }
}
