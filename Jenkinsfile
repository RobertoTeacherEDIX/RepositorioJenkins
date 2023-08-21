pipeline {
agent any
     triggers { cron('* * * * *') }
     options { timeout(time: 5) }
     parameters { 
          booleanParam(name: "MOSTRAR_STEP", defaultValue: true, 
          description: "QUIERES EJECUTAR EL CODIGO?") 
     }
stages {
 stage("Primer_Stage") {
          environment { NAME = "ROBER" }
          when { expression { return params.MOSTRAR_STEP} } 
    steps {
        echo "Step 1. HOLA ${NAME}. SE EJECUTA EL CODIGO DEL STEP 1"
            }
    }
 stage("Segundo_Stage") {
    steps {
        echo "Step 2." 
        echo "Step 3."
        }
    }
}
post { always { echo "Fin del pipeline" } }
}
