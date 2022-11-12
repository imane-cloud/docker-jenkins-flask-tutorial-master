node {
    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'dockerHub') {

        def customImage = docker.build("ad825d70b9ed")

        /* Push the container to the custom Registry */
        registry = "dockerimanehiba/ad825d70b9ed"
        registryCredential = 'dockerHub'
        dockerImage = 'ad825d70b9ed'
        docker.withRegistry( '', registryCredential ) {
        customImage.push()
      }
        
    }
}
