@library('https://github.com/RobertoTeacherEDIX/RepositorioJenkins/tree/main/MisLibrerias')
pipeline {
    agent none
    stages {
        stage('Stage crea contenedor') {
		    agent {
			    script {
                    LibreriaContenedor()
                }
			}
           	steps {
                	echo 'Stage con ejecución normal'
			        sh 'node --version'
           		 }
        }
   	}
post { always { echo "Fin del pipeline" } }
}

