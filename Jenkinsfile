node {

    stage('Clonar GitLab') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }

    stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */

        app = docker.build("customphp")
    }
    stage('Correr el contenedor'){
	sh 'docker run -d --name apache -p 81:80 customphp'
	}
}
