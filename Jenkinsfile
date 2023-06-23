
pipeline {
    agent any
    
    stages {
        stage('Clonar Repositorio') {
            steps {
                // Clonar el repositorio de GitHub en la carpeta temporal
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/rbrenesr/edu-bootstrap5.git']]])
            }
        }
        
        stage('Copiar archivos') {
            steps {
                // Copiar los archivos del repositorio a una carpeta en disco C
                bat 'xcopy /E /I /Y %TEMP% C:\\Sites\\temp'
            }
        }
    }
}
