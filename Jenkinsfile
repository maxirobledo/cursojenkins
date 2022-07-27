pipeline {
    agent any 
    environment{
        NOMBRE = 'Maximiliano'
        APELLIDO = 'Robledo'
        U1_CREDENTIALS = credentials('usuario1')
    }
    stages {
        stage('Build') { 
            steps {                
		        sh '''
                	echo "Pasos múltiples de shell también funcionan"
                    echo "Consultor DevOps Jr. - $NOMBRE $APELLIDO"
                    echo "Mis credenciales son $U1_CREDENTIALS_USR y password $U1_CREDENTIALS_PSW"
             	'''
            }
        }
        stage('Test') { 
            steps {
                sh 'echo "Arranca el proceso de pruebas unitarias" '
            }
        }
        stage('Deploy') { 
            steps {
                sh 'echo "Desplegando al área de desarrollo" '  
            }
        }
    }
}
