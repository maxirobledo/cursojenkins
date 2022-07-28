pipeline {
    agent any
    parameters {
        string(name: 'PERSONA', defaultValue: 'Julian', description: 'A quien debo saludar?')

        booleanParam(name: 'FLAG', defaultValue: true, description: 'FLAG Verdadera?')

        choice(name: 'Eleccion', choices: ['A', 'B', 'C'], description: 'Elegir una opción')
    }
    stages {
        stage('Clase de Parametros') {
            steps {
                echo "Hola, como estas ${params.PERSONA}"

                echo "FLAG: ${params.FLAG}"

                echo "Eleccion: ${params.Eleccion}"
            }
        }
    }
}
