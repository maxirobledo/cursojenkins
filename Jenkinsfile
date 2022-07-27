pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {                
		sh '''
                	echo "Pasos múltiples de shell también funcionan"
			pwd
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
