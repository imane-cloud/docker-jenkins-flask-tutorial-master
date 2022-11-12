node {
    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'dockerHub') {

        def customImage = docker.build("ad825d70b9ed")

        /* Push the container to the custom Registry */
        docker.withRegistry( '', registryCredential ) {
        customImage.push()
      }
        
    }
}
