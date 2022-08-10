pipeline {
    agent any
    options {
        timeout(time: 60, unit: 'SECONDS') 
    }
    stages {
        stage('Etapa 1') { 
            steps {
                echo "Arranca la Etapa 1" 		     
		            sh 'sleep 10'
		    }
	    }
        stage('Etapa 2') {
            input {
                message "Continuar el proyecto?"
                ok "Continuar"
                parameters {
                    string(name: 'PERSONA', defaultValue: 'Julian', description: 'A quien debo saludar?')
                }
            }
            steps {
                echo "Hola, ${PERSONA}, un placer conocerte."
            }
        }
    }
    post { 
        success{
            echo 'Esta ejecución ha finalizado exiitosamente'
        }
        aborted{
            echo 'Esta ejecución se ha abortado'
        }
        failure { 
            echo 'Esta ejecución ha fallado'
        }
    }
}

