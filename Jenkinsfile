node {
    checkout scm
    def app
    stage('Building Image'){
        app =  docker.build("php-apache:latest")
    }
    stage('Push Image to Docker REgistry'){
        docker.withRegistry('https://registry.hubn.docker.com','dockerhub-creds'){
            app.push()
        }
    }
}
