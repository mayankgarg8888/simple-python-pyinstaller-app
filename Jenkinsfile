node {
    checkout scm

    docker.withRegistry('https://gitlab.spay.com:4567', '1152810a-b80e-4786-bf89-45b6fc6c31fb') {

        def customImage = docker.build("my-image:${env.BUILD_ID}")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}
}
