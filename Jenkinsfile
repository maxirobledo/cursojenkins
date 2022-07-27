pipeline {
    agent any 
    environment{
        NOMBRE = 'Maximiliano'
        APELLIDO = 'Robledo'
        DH_CREDENTIALS = credentials('dockerhub')
    }
    stages {
        stage('Build') { 
            steps {                
		        sh '''
                	echo "Pasos múltiples de shell también funcionan"
                    echo "Consultor DevOps Jr. - $NOMBRE $APELLIDO"
                    echo "Mis credenciales son $DH_CREDENTIALS"
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
