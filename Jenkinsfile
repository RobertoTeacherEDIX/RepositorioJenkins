@Library('github.com/RobertoTeacherEDIX/RepositorioLibrerias@main') _

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

