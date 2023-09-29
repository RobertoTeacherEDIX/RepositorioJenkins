@Library('github.com/RobertoTeacherEDIX/RepositorioLibrerias@main') _

pipeline {
    agent none
    stages {
        stage('Stage crea contenedor') {
		    agent {
			docker { image 'node:20-alpine' }
                	}
           	    steps {
                	echo 'Stage con ejecución normal'
				LibreriaContenedor()
		    	  }
	}
        }
post { always { echo "Fin del pipeline" } }
}

