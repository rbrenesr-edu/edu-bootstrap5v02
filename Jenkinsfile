pipeline {
    agent any
    
    stages {
        stage('Clonar repositorio') {
            steps {
                // Clonar el repositorio de GitHub en el directorio de trabajo
                git 'https://github.com/rbrenesr/edu-bootstrap5.git'
            }
        }
        
        stage('Copiar archivos') {
            steps {
                // Crear una carpeta en el disco local
                bat 'mkdir C:\\Sites\\temp'
                
                // Copiar los archivos al directorio de destino
                bat 'xcopy /Y /I . C:\\Sites\\temp'
            }
        }
    }
}
