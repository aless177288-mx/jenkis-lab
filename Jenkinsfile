pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Código descargado desde GitHub'
            }
        }

        stage('Verificar archivos') {
            steps {
                sh 'ls -la'
            }
        }

        stage('Ejecutar script') {
            steps {
                sh '''
                    chmod +x hola.sh
                    ./hola.sh
                '''
            }
        }
    }

    post {
        success {
            echo 'Pipeline terminado correctamente'
        }

        failure {
            echo 'El pipeline falló'
        }
    }
}
