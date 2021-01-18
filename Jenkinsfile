node {
    checkout scm
    def app
    stage('Building Image'){
        app =  docker.build("salakhaliffjr/php-apache-plain:latest")
    }
    stage('Push Image to Docker REgistry'){
        docker.withRegistry('https://registry.hub.docker.com','dockerhub-creds'){
            app.push("latest")
        }
    }
}
